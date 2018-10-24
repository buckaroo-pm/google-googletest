cxx_library(
  name = 'gtest',
  header_namespace = '',
  srcs = [
    'googletest/src/gtest-all.cc',
    'googletest/src/gtest_main.cc',
  ],
  headers = subdir_glob([
    ('googletest', 'src/*.h'),
    ('googletest', 'src/*.cc'),
    ('googletest/include', 'internal/**/*.h'),
  ]),
  exported_headers = subdir_glob([
    ('googletest/include', '**/*.h'),
  ], excludes = [
    'googletest/include/internal/**/*.h',
  ]),
  preprocessor_flags = [
    '-U_STRICT_ANSI_',
  ],
  compiler_flags = [
    '-std=c++14',
  ],
  platform_compiler_flags = [
    ('linux.*', [ '-pthread' ]), 
  ], 
  exported_platform_linker_flags = [
    ('^linux.*', [ '-lpthread' ]),
  ],
  visibility = [
    'PUBLIC',
  ],
)
