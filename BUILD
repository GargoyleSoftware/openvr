package(default_visibility = ["//visibility:public"])

cc_import(
    name = "bin",
    static_library = "lib/win64/openvr_api.lib",
    shared_library = "bin/win64/openvr_api.dll",
    # Linux
    #"lib/linux64/libopenvr_api.so"
    #"bin/linux64/libopenvr_api.so"

    #hdrs = glob([ "headers/*.h" ]), [
    #hdrs = [ 'headers/openvr_capi.h', 'headers/openvr_driver.h', 'headers/openvr.h', #'headers/openvr_api.cs', #'headers/openvr_api.json', ],
    # deps = [ ':hdrs', ],
  )

cc_library(
    name = "libopenvr_api",
    hdrs = [
      'headers/openvr_capi.h',
      'headers/openvr_driver.h',
      'headers/openvr.h',
    ],
    includes = [
        'headers',
    ],
    strip_include_prefix = "headers",
    deps = [
        ':bin',
    ],
    )


