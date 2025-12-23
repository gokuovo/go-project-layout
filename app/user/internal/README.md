# `/internal`

私有应用程序和库代码。这是您不希望他人在其应用程序或库中导入的代码。请注意，这种布局模式由 Go 编译器本身强制执行。有关更多详细信息，请参阅 Go 1.4 [`发布说明`](https://golang.org/doc/go1.4#internalpackages)。请注意，您不仅限于顶级 `internal` 目录。您可以在项目树的任何级别拥有多个 `internal` 目录。

您可以选择为内部包添加一些额外的结构，以分离共享和非共享的内部代码。这不是必需的（特别是对于较小的项目），但通过视觉线索显示预期的包用途是很有好处的。您的实际应用程序代码可以放在 `/internal/app` 目录（例如 `/internal/app/myapp`），而这些应用程序共享的代码可以放在 `/internal/pkg` 目录（例如 `/internal/pkg/myprivlib`）。

示例：

* https://github.com/hashicorp/terraform/tree/main/internal
* https://github.com/influxdata/influxdb/tree/master/internal
* https://github.com/perkeep/perkeep/tree/master/internal
* https://github.com/jaegertracing/jaeger/tree/main/internal
* https://github.com/moby/moby/tree/master/internal
* https://github.com/satellity/satellity/tree/main/internal
* https://github.com/minio/minio/tree/master/internal

## `/internal/pkg`

示例：

* https://github.com/hashicorp/waypoint/tree/main/internal/pkg
