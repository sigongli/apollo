load("//tools:cpplint.bzl", "cpplint")

package(default_visibility = ["//visibility:public"])

cc_library(
    name = "bare_intersection_unprotected_scenario",
    srcs = [
        "bare_intersection_unprotected_scenario.cc",
        "stage_approach.cc",
        "stage_intersection_cruise.cc",
    ],
    hdrs = [
        "bare_intersection_unprotected_scenario.h",
        "stage_approach.h",
        "stage_intersection_cruise.h",
    ],
    copts = ["-DMODULE_NAME=\\\"planning\\\""],
    deps = [
        "//cyber/common:log",
        "//external:gflags",
        "//modules/common",
        "//modules/common/util",
        "//modules/common/util:factory",
        "//modules/planning/proto:planning_proto",
        "//modules/planning/scenarios:scenario",
        "//modules/planning/scenarios:stage_intersection_cruise_impl",
        "//modules/planning/tasks/deciders:decider",
        "@eigen",
    ],
)

cc_test(
    name = "bare_intersection_unprotected_scenario_test",
    size = "small",
    srcs = ["bare_intersection_unprotected_scenario_test.cc"],
    data = ["//modules/planning:planning_conf"],
    deps = [
        ":bare_intersection_unprotected_scenario",
        "@gtest//:main",
    ],
)

cpplint()
