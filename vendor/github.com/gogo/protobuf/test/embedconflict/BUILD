load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

filegroup(
    name = "go_default_library_protos",
    srcs = [
        "eb.proto",
        "ec.proto",
        "ee.proto",
        "em.proto",
        "en.proto",
        "er.proto",
    ],
    visibility = ["//visibility:public"],
)

go_library(
    name = "go_default_library",
    srcs = ["doc.go"],
    importpath = "github.com/gogo/protobuf/test/embedconflict",
    visibility = ["//visibility:public"],
)

go_test(
    name = "go_default_test",
    srcs = ["ec_test.go"],
    importpath = "github.com/gogo/protobuf/test/embedconflict",
    library = ":go_default_library",
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
