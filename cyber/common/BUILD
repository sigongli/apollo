load("//tools:cpplint.bzl", "cpplint")

package(default_visibility = ["//visibility:public"])

cc_library(
    name = "common",
    deps = [
        "//cyber/common:environment",
        "//cyber/common:file",
        "//cyber/common:global_data",
        "//cyber/common:log",
        "//cyber/common:macros",
        "//cyber/common:time_conversion",
        "//cyber/common:types",
        "//cyber/common:util",
    ],
)

cc_library(
    name = "file",
    srcs = [
        "file.cc",
    ],
    hdrs = [
        "file.h",
    ],
    deps = [
        "//cyber/common:log",
    ],
)

cc_test(
    name = "file_test",
    size = "small",
    srcs = [
        "file_test.cc",
    ],
    deps = [
        "//cyber",
        "//cyber/proto:unit_test_cc_proto",
        "@gtest//:main",
    ],
)

cc_library(
    name = "log",
    hdrs = [
        "log.h",
    ],
    linkopts = [
        "-lglog",
    ],
    deps = [
        "//cyber:binary",
    ],
)

cc_test(
    name = "log_test",
    size = "small",
    srcs = [
        "log_test.cc",
    ],
    deps = [
        "//cyber",
        "@gtest//:main",
    ],
)

cc_library(
    name = "environment",
    hdrs = [
        "environment.h",
    ],
)

cc_library(
    name = "global_data",
    srcs = [
        "global_data.cc",
    ],
    hdrs = [
        "global_data.h",
    ],
    deps = [
        "//cyber/base:atomic_hash_map",
        "//cyber/base:atomic_rw_lock",
        "//cyber/common:environment",
        "//cyber/common:file",
        "//cyber/common:macros",
        "//cyber/common:util",
        "//cyber/proto:cyber_conf_cc_proto",
    ],
)

cc_test(
    name = "macros_test",
    size = "small",
    srcs = [
        "macros_test.cc",
    ],
    deps = [
        "//cyber",
        "@gtest//:main",
    ],
)

cc_library(
    name = "macros",
    hdrs = [
        "macros.h",
    ],
    deps = [
        "//cyber/base:macros",
    ],
)

cc_library(
    name = "time_conversion",
    hdrs = [
        "time_conversion.h",
    ],
)

cc_library(
    name = "types",
    hdrs = [
        "types.h",
    ],
)

cc_library(
    name = "util",
    hdrs = [
        "util.h",
    ],
)

cpplint()
