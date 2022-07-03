project(
  'gbm_gralloc', 'cpp',
  version : '1.0.0',
  meson_version : '>= 0.53.0',
  default_options : ['warning_level=1'])

# android stub libs required
deps = []
foreach lib : ['libdrm', 'gbm', 'log', 'cutils', 'hardware']
  deps += dependency(lib)
endforeach

cpp_args = get_option('cpp_args') + ['-DNDEBUG']

shared_library(
  'gralloc.gbm',
  name_prefix : '',
  cpp_args: cpp_args,
  sources : ['gralloc.cpp', 'gralloc_gbm.cpp'],
  install : true,
  install_dir: join_paths(get_option('libdir'), 'hw'),
  dependencies : deps,
)
