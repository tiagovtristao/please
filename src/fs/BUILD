go_library(
    name = "fs",
    srcs = glob(
        ["*.go"],
        exclude = ["*_test.go"],
    ),
    visibility = ["PUBLIC"],
    deps = [
        "//src/process",
        "//third_party/go:godirwalk",
        "//third_party/go:logging",
        "//third_party/go:xattr",
    ],
)

go_test(
    name = "fs_test",
    srcs = glob(
        ["*_test.go"],
        exclude = ["glob_integration_test.go"],
    ),
    data = ["test_data"],
    deps = [
        ":fs",
        "//third_party/go:testify",
    ],
)

go_test(
    name = "glob_integration_test",
    srcs = ["glob_integration_test.go"],
    # This must remain a glob because the tests rely on data being loaded in via globs
    data = glob(["test_data/**"]),
)
