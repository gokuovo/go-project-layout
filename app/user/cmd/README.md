# `/cmd`

项目的主要应用程序。

每个应用程序的目录名称应与您想要的可执行文件名称相匹配（例如，`/cmd/myapp`）。

不要在应用程序目录中放入太多代码。如果您认为代码可以被导入并在其他项目中使用，那么它应该放在 `/pkg` 目录中。如果代码不可重用，或者如果您不希望他人重用它，请将该代码放在 `/internal` 目录中。您会对别人的做法感到惊讶，所以请明确您的意图！

通常会有一个小的 `main` 函数，它从 `/internal` 和 `/pkg` 目录导入并调用代码，除此之外别无他法。

示例：

* https://github.com/vmware-tanzu/velero/tree/main/cmd (just a really small `main` function with everything else in packages)
* https://github.com/moby/moby/tree/master/cmd
* https://github.com/prometheus/prometheus/tree/main/cmd
* https://github.com/influxdata/influxdb/tree/master/cmd
* https://github.com/kubernetes/kubernetes/tree/master/cmd
* https://github.com/dapr/dapr/tree/master/cmd
* https://github.com/ethereum/go-ethereum/tree/master/cmd
