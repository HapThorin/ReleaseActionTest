# ReleaseActionTest

使用`Github Action`自动发布`release`的示例。本示例主要使用[create-release](https://github.com/actions/create-release)发布`release`版本，使用[upload-release-asset](https://github.com/actions/upload-release-asset)上传`release`包。

确保`.github/workflows`目录中配置有相关的工作流，示例见[release.yml](./.github/workflows/release.yml)。

执行以下命令创建tag
```shell
git tag -a "${tag_name}" -m "${release_message}"
```

执行以下命令推送tag至远端仓库
```shell
git push --tags
```

之后便会生成一个`Github Action`，运行完毕后，将自动发布一个`release`。
