load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "doc.go",
        "types.go",
        "zz_generated.deepcopy.go",
    ],
    importmap = "k8s.io/kubernetes/vendor/k8s.io/apimachinery/pkg/apis/config",
    importpath = "k8s.io/apimachinery/pkg/apis/config",
    visibility = ["//visibility:public"],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [
        ":package-srcs",
        "//staging/src/k8s.io/apimachinery/pkg/apis/config/v1alpha1:all-srcs",
        "//staging/src/k8s.io/apimachinery/pkg/apis/config/validation:all-srcs",
    ],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
