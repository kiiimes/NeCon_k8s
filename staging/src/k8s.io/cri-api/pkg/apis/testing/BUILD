load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "fake_image_service.go",
        "fake_runtime_service.go",
        "utils.go",
    ],
    importmap = "k8s.io/kubernetes/vendor/k8s.io/cri-api/pkg/apis/testing",
    importpath = "k8s.io/cri-api/pkg/apis/testing",
    visibility = ["//visibility:public"],
    deps = [
        "//staging/src/k8s.io/cri-api/pkg/apis/runtime/v1alpha2:go_default_library",
        "//vendor/github.com/stretchr/testify/assert:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
