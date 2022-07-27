package(default_visibility = ["//visibility:public"])

objc_library(
    name = "GoogleUtilities",
    copts = [
        "-std=c99",
    ],
    module_name = "GoogleUtilities",
    deps = [
        ":AppDelegateSwizzler",
        ":Environment",
        ":Logger",
        ":NSData",
    ],
)

objc_library(
    name = "Environment",
    srcs = glob([
        "GoogleUtilities/Environment/**/*.m",
        "GoogleUtilities/Environment/**/*.h",
    ]),
    hdrs = glob([
        "GoogleUtilities/Environment/Public/**/*.h",
    ]),
    includes = [
        "GoogleUtilities/Environment/Public",
    ],
    sdk_frameworks = [
        "Security",
    ],
    deps = [
        "@Promises//:FBLPromises",
    ],
)

objc_library(
    name = "Logger",
    srcs = glob([
        "GoogleUtilities/Logger/**/*.m",
        "GoogleUtilities/Logger/**/*.h",
    ]),
    hdrs = glob([
        "GoogleUtilities/Logger/**/*.h",
    ]),
    includes = [
        "GoogleUtilities/Logger/Public",
    ],
    deps = [
        ":Environment",
    ],
)

objc_library(
    name = "NSData",
    srcs = glob([
        "GoogleUtilities/NSData+zlib/**/*.h",
        "GoogleUtilities/NSData+zlib/**/*.m",
    ]),
    hdrs = glob([
        "GoogleUtilities/NSData+zlib/Public/GoogleUtilities/**/*.h",
    ]),
    includes = [
        "GoogleUtilities/NSData+zlib/Public",
    ],
    module_name = "GoogleUtilities_NSData",
    sdk_dylibs = [
        "libz",
    ],
)

objc_library(
    name = "Reachability",
    srcs = glob([
        "GoogleUtilities/Reachability/**/*.h",
        "GoogleUtilities/Reachability/**/*.m",
    ]),
    hdrs = glob([
        "GoogleUtilities/Reachability/Public/GoogleUtilities/**/*.h",
    ]),
    includes = [
        "GoogleUtilities/Reachability/Public",
    ],
    sdk_dylibs = [
        "SystemConfiguration",
    ],
    deps = [
        ":Logger",
    ],
)

objc_library(
    name = "Network",
    srcs = glob([
        "GoogleUtilities/Network/**/*.h",
        "GoogleUtilities/Network/**/*.m",
    ]),
    hdrs = glob([
        "GoogleUtilities/Network/Public/GoogleUtilities/**/*.h",
    ]),
    includes = [
        "GoogleUtilities/Network/Public",
    ],
    sdk_dylibs = [
        "Security",
    ],
    deps = [
        ":Logger",
        ":NSData",
        ":Reachability",
    ],
)

objc_library(
    name = "AppDelegateSwizzler",
    srcs = glob([
        "GoogleUtilities/AppDelegateSwizzler/Internal/**/*.h",
        "GoogleUtilities/AppDelegateSwizzler/Public/**/*.h",
        "GoogleUtilities/AppDelegateSwizzler/**/*.m",
        "GoogleUtilities/Common/**/*.h",
    ]),
    hdrs = glob([
        "GoogleUtilities/AppDelegateSwizzler/Public/GoogleUtilities/**/*.h",
    ]),
    enable_modules = True,
    includes = [
        "GoogleUtilities/AppDelegateSwizzler/Public",
    ],
    deps = [
        ":Environment",
        ":Logger",
        ":Network",
    ],
)
