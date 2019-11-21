load("@bazel_skylib//:bzl_library.bzl", "bzl_library")

package(default_visibility = ["//visibility:public"])

exports_files(["codegen_template"])

bzl_library(
    name = "_codegen_action",
    srcs = ["_codegen_action.bzl"],
    visibility = ["//visibility:private"],
    deps = [
        "//dart/build_rules/common:constants",
        "//dart/build_rules/internal:common",
    ],
)

bzl_library(
    name = "_codegen_aspect",
    srcs = ["_codegen_aspect.bzl"],
    visibility = ["//visibility:private"],
)

bzl_library(
    name = "_codegen_binary",
    srcs = ["_codegen_binary.bzl"],
    visibility = ["//visibility:private"],
    deps = [
        ":_labels",
        "//dart/build_rules:vm",
        "//dart/build_rules/internal:common",
        "@bazel_skylib//lib:dicts",
    ],
)

bzl_library(
    name = "_codegen_rule",
    srcs = ["_codegen_rule.bzl"],
    visibility = ["//visibility:private"],
    deps = [
        ":_codegen_action",
        "//dart/build_rules/internal:common",
    ],
)

bzl_library(
    name = "_labels",
    srcs = ["_labels.bzl"],
    visibility = ["//visibility:private"],
)

bzl_library(
    name = "codegen",
    srcs = ["codegen.bzl"],
    deps = [
        ":_codegen_action",
        ":_codegen_aspect",
        ":_codegen_binary",
        ":_codegen_rule",
    ],
)
