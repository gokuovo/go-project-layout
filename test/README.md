# `/test`

额外的外部测试应用程序和测试数据。您可以随意构建 `/test` 目录。对于较大的项目，拥有一个数据子目录是有意义的。例如，如果您需要 Go 忽略该目录中的内容，可以使用 `/test/data` 或 `/test/testdata`。请注意，Go 还会忽略以 “.” 或 “_” 开头的目录或文件，因此您在命名测试数据目录方面有更大的灵活性。

示例：

* https://github.com/openshift/origin/tree/master/test (test data is in the `/testdata` subdirectory)


