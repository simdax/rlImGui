project('rlImgui', 'cpp',
  version : '0.1',
  default_options : ['warning_level=3', 'cpp_std=c++14'])

lib = static_library('rlImgui',
           'rlImGui.cpp',
           dependencies: [
            subproject('core').get_variable('dep'),
            subproject('imgui').get_variable('imgui_dep'),
           ]
    )

dep = declare_dependency(
    include_directories: '.',
    link_with: lib,
    dependencies: [
        subproject('imgui').get_variable('imgui_dep'),
    ]
)
