project('rlImgui', 'cpp',
  version : '0.1',
  default_options : [
    'warning_level=3',
    ])

cmake = import('cmake')

options = cmake.subproject_options()
options.add_cmake_defines(
  {'CUSTOMIZE_BUILD': 'ON',
    'BUILD_SHARED_LIBS': 'ON',
  })
raylib = cmake.subproject('raylib', options: options,
  )

lib = static_library('rlImgui',
           'rlImGui.cpp',
           dependencies: [
            raylib.dependency('raylib', 
              ),
            subproject('imgui').get_variable('imgui_dep'),
           ],
    )

dep = declare_dependency(
    include_directories: '.',
    link_with: lib,
    dependencies: [
        raylib.dependency('raylib'),
        subproject('imgui').get_variable('imgui_dep'),
    ]
)
