project(
  'gbm_gralloc', 'cpp',
  version : '1.0.0',
  meson_version : '>= 0.53.0',
  default_options : ['buildtype=debugoptimized',
    'b_ndebug=if-release', 'c_std=c99', 'cpp_std=c++14'])

# android stub libs required
deps = []
foreach lib : ['libdrm', 'gbm', 'log', 'cutils', 'hardware']
  deps += dependency(lib)
endforeach

shared_library(
  'gralloc.gbm',
  name_prefix : '',
  sources : ['gralloc.cpp', 'gralloc_gbm.cpp'],
  install : true,
  install_dir: get_option('libdir') / 'hw',
  dependencies : deps,
)
