load("@bazel_skylib//:bzl_library.bzl", "bzl_library")

package(default_visibility = ["//visibility:public"])

bzl_library(
    name = "analyze",
    srcs = ["analyze.bzl"],
    deps = [
        ":common",
    ],
)

bzl_library(
    name = "common",
    srcs = ["common.bzl"],
    deps = [
        "//dart/build_rules/common:constants",
        "//dart/build_rules/common:context",
        "//dart/build_rules/common:ddc",
        "//dart/build_rules/common:label",
        "//dart/build_rules/common:path",
    ],
)

bzl_library(
    name = "dart2js",
    srcs = ["dart2js.bzl"],
    deps = [
        ":common",
    ],
)

bzl_library(
    name = "dart_library",
    srcs = ["dart_library.bzl"],
    deps = [
        ":analyze",
        ":common",
        ":ddc",
    ],
)

bzl_library(
    name = "dart_vm_binary",
    srcs = ["dart_vm_binary.bzl"],
    deps = [
        ":common",
        ":dart_vm_snapshot",
    ],
)

bzl_library(
    name = "dart_vm_snapshot",
    srcs = ["dart_vm_snapshot.bzl"],
    deps = [
        ":common",
    ],
)

bzl_library(
    name = "dart_vm_test",
    srcs = ["dart_vm_test.bzl"],
    deps = [
        ":common",
    ],
)

bzl_library(
    name = "dart_web_application",
    srcs = ["dart_web_application.bzl"],
    deps = [
        ":common",
        ":dart2js",
    ],
)

bzl_library(
    name = "ddc",
    srcs = ["ddc.bzl"],
    deps = [
        ":common",
    ],
)

bzl_library(
    name = "pub",
    srcs = ["pub.bzl"],
)

bzl_library(
    name = "sdk",
    srcs = ["sdk.bzl"],
)
