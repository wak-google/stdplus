stdplus_headers = include_directories('.')

stdplus_lib = library(
  'stdplus',
  [
    'stdplus/signal.cpp',
  ],
  include_directories: stdplus_headers,
  implicit_include_directories: false,
  version: meson.project_version(),
  install: true)

stdplus = declare_dependency(
  include_directories: stdplus_headers,
  link_with: stdplus_lib)

import('pkgconfig').generate(
  name: 'stdplus',
  description: 'C++ helper utilities',
  version: meson.project_version(),
  libraries: stdplus)

install_headers(
  'stdplus/signal.hpp',
  subdir: 'stdplus')

install_headers(
  'stdplus/handle/copyable.hpp',
  'stdplus/handle/managed.hpp',
  subdir: 'stdplus/handle')

install_headers(
  'stdplus/util/cexec.hpp',
  'stdplus/util/string.hpp',
  subdir: 'stdplus/util')
