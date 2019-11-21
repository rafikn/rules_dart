load("@bazel_skylib//:bzl_library.bzl", "bzl_library")

package(default_visibility = ["//visibility:public"])

bzl_library(
    name = "core",
    srcs = ["core.bzl"],
    deps = [
        "//dart/build_rules/internal:dart_library",
    ],
)

bzl_library(
    name = "vm",
    srcs = ["vm.bzl"],
    deps = [
        "//dart/build_rules/internal:dart_vm_binary",
        "//dart/build_rules/internal:dart_vm_snapshot",
        "@bazel_skylib//lib:dicts",
    ],
)

bzl_library(
    name = "web",
    srcs = ["web.bzl"],
    deps = [
        ":vm",
        "//dart/build_rules/internal:dart_web_application",
        "//dart/build_rules/internal:ddc",
    ],
)
