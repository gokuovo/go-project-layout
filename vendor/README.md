# `/vendor`

应用程序依赖项（通过手动管理、您喜欢的依赖项管理工具或内置的 [`modules`](https://go.dev/wiki/Modules) 功能进行管理）。

如果您正在构建库，请不要提交应用程序依赖项。

请注意，自 [`1.13`](https://golang.org/doc/go1.13#modules) 起，Go 还启用了模块代理功能（默认使用 `https://proxy.golang.org` 作为其模块代理服务器）。在[`这里`](https://blog.golang.org/module-mirror-launch)阅读更多相关信息，看看它是否符合您的所有要求和约束。如果是，那么您根本不需要 'vendor' 目录。
