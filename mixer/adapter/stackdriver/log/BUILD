load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = ["log.go"],
    visibility = ["//visibility:public"],
    deps = [
        "//mixer/adapter/stackdriver/config:go_default_library",
        "//mixer/adapter/stackdriver/helper:go_default_library",
        "//mixer/pkg/adapter:go_default_library",
        "//mixer/pkg/pool:go_default_library",
        "//mixer/template/logentry:go_default_library",
        "@com_google_cloud_go//logging:go_default_library",
        "@org_golang_google_api//option:go_default_library",
        "@org_golang_google_genproto//googleapis/api/monitoredres:go_default_library",
        "@org_golang_x_net//context:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["log_test.go"],
    library = ":go_default_library",
    deps = [
        "//mixer/adapter/stackdriver/config:go_default_library",
        "//mixer/pkg/adapter/test:go_default_library",
        "//mixer/template/logentry:go_default_library",
        "@com_google_cloud_go//logging:go_default_library",
        "@org_golang_google_api//option:go_default_library",
        "@org_golang_google_genproto//googleapis/api/monitoredres:go_default_library",
        "@org_golang_x_net//context:go_default_library",
    ],
)
