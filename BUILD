package(default_visibility = ["//visibility:public"])

cc_library(
    name = "libopenvr_api",
    srcs = [
        "lib/linux64/libopenvr_api.so"
        #"bin/linux64/libopenvr_api.so"
        ],
    #hdrs = glob([ "headers/*.h" ]), [
    hdrs = [
      'headers/openvr_capi.h',
      'headers/openvr_driver.h',
      'headers/openvr.h',
      #'headers/openvr_api.cs',
      #'headers/openvr_api.json',
    ],

    copts = [
        #"-I.",
        #"-Isubprojects/ogre2/Samples/2.0/Tutorials/Tutorial04",
        #"-Isubprojects/ogre2/Samples/2.0/Tutorials/headers",
        #"-Isubprojects/ogre2/Samples/2.0/Common/include",
        #"-Isubprojects/ogre2/OgreMain/include",
        #"-Isubprojects/ogre2/Components/Hlms/Common/include",
        #"-Isubprojects/ogre2/Components/Hlms/Unlit/include",
        #"-Isubprojects/ogre2/Components/Hlms/Pbs/include",
        #"-isystem/usr/include/SDL2",
    ],
    # linkopts = [ ],
    # deps = [ ],
  )

