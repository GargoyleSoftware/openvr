project('libopenvr_api', 'cpp',
  default_options : [
      ])

cpp_src = [
  'src/openvr_api_public.cpp',
  'src/jsoncpp.cpp',
  'src/vrcommon/dirtools_public.cpp',
  'src/vrcommon/envvartools_public.cpp',
  'src/vrcommon/hmderrors_public.cpp',
  'src/vrcommon/pathtools_public.cpp',
  'src/vrcommon/sharedlibtools_public.cpp',
  'src/vrcommon/strtools_public.cpp',
  'src/vrcommon/vrpathregistry_public.cpp',
]

add_project_arguments(
    '-std=c++11',
    '-fPIC',
    '-fvisibility=hidden',
    #'-stdlib=libc++',
    '-w',
    '-DVR_API_PUBLIC',
    '-DLINUX',
    '-DLINUX64',
    '-DPOSIX',
    language : 'cpp')

cc = meson.get_compiler('cpp')
inc = include_directories(
    'src',
    'src/vrcommon',
    'headers'
  )

libopenvr_api = library('openvr_api', cpp_src,
  link_with: [

  ],
  dependencies: [
    cc.find_library('dl'),
  ],

  include_directories: inc
  )

libopenvr_api_dep = declare_dependency(include_directories: inc,
  link_with: libopenvr_api)
