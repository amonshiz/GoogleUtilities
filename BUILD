package(default_visibility = ["//visibility:public"])

objc_library(
    name = "GoogleUtilities",
    copts = [
        "-std=c99",
    ],
    includes = [
        "./",
    ],
    module_name = "GoogleUtilities",
    deps = [
        ":Environment",
        ":Logger",
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
