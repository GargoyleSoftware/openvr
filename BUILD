package(default_visibility = ["//visibility:public"])

cc_import(
    name = "win32dep",
    interface_library = "lib/win64/openvr_api.lib",
    shared_library    = "bin/win64/openvr_api.dll",
    )

cc_library(
    name = "linuxdep",
    hdrs = [ ],
    srcs = [ "lib/linux64/libopenvr_api.so", ],
    )

cc_library(
    name = "openvr_api",
    hdrs = [
      'headers/openvr_capi.h',
      'headers/openvr_driver.h',
      'headers/openvr.h',
    ],
    includes = [
        'headers',
    ],
    strip_include_prefix = "headers",
    deps = select({
        "//platforms:linux": [ ':linuxdep' ],
        "//platforms:win32": [ ':win32dep' ],
        })
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
    deps = select({
        "//platforms:linux": [ ':linuxdep' ],
        "//platforms:win32": [ ':win32dep' ],
        })
    )
