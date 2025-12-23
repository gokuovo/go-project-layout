# `/build`

打包和持续集成。

将您的云（AMI）、容器（Docker）、操作系统（deb、rpm、pkg）包配置和脚本放在 `/build/package` 目录中。

将您的 CI（travis、circle、drone）配置和脚本放在 `/build/ci` 目录中。请注意，某些 CI 工具（例如 Travis CI）对其配置文件的位置非常挑剔。如果可能，请尝试将配置文件放在 `/build/ci` 目录中，并将它们链接到 CI 工具期望的位置（如果不行，或者如果将这些文件保留在根目录中使您的生活更轻松，请不要担心 :-)）。

示例：

* https://github.com/cockroachdb/cockroach/tree/master/build
