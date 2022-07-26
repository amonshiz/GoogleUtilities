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
        "GoogleUtilities/Environment/**/*.h",
    ]),
    includes = glob([
        "GoogleUtilities/Environment/Public/GoogleUtilities/**/*.h",
    ]),
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
        "GoogleUtilities/Logger/Public/GoogleUtilities",
    ],
    deps = [
        ":Environment",
    ],
)
