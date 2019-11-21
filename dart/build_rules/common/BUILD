load("@bazel_skylib//:bzl_library.bzl", "bzl_library")

package(default_visibility = ["//visibility:public"])

bzl_library(
    name = "_archive",
    srcs = ["_archive.bzl"],
)

bzl_library(
    name = "constants",
    srcs = ["constants.bzl"],
)

bzl_library(
    name = "context",
    srcs = ["context.bzl"],
    deps = [
        ":_archive",
        ":constants",
        ":path",
        "//dart/build_rules/common:ddc",
        "//dart/build_rules/common:label",
    ],
)

bzl_library(
    name = "ddc",
    srcs = ["ddc.bzl"],
)

bzl_library(
    name = "label",
    srcs = ["label.bzl"],
)

bzl_library(
    name = "package_spec",
    srcs = ["package_spec.bzl"],
    deps = [
        ":context",
        ":path",
    ],
)

bzl_library(
    name = "kernel",
    srcs = ["kernel.bzl"],
    deps = [
        ":package_spec",
        ":path",
        "//dart/build_rules/internal:common",
    ],
)

# TODO(@Capstan): path -> @bazel_skylib//:lib.bzl paths
bzl_library(
    name = "path",
    srcs = ["path.bzl"],
)
