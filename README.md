# Window Pet

把小挂件挂在打开的窗口上，让它随着窗口移动自然摆动。

## 下载

[下载 Windows v0.0.1](https://github.com/supremejohnny/windowWidget/releases/download/v0.0.1/WindowPet-0.0.1.exe) · [查看 Release](https://github.com/supremejohnny/windowWidget/releases/tag/v0.0.1)

单个 EXE，双击即可启动，无需安装或额外资源文件夹。

## 使用

1. 选择要挂载的窗口和挂件。
2. 选择左上 / 右上 / 左下 / 右下，以及短 / 中 / 长 / 超长绳子。
3. 点击 **Attach** 开始挂载。
4. 点击挂件可以戳动；点击锚点可以收起或展开。
5. **Detach** 解除挂载；关闭设置窗口退出程序。

## 特点

- 自然的绳子弯曲与挂件摆动。
- 固定锚点；收起后留下短绳。
- 其他窗口正常遮挡挂件，透明区域不阻挡点击。
- 内置三款简绘挂件和 `amiya_test1` 测试角色。
- 轻量运行：本机观察私有工作集约 14 MiB；用户反馈连续运行约 2.5 小时，占用正常、无卡顿。实际占用随环境变化。

## 兼容性

面向 Windows 10 / 11，使用系统 .NET Framework。当前完整验证环境为 Windows 10 22H2 x64；Windows 11、ARM64、混合 DPI 多屏和特殊窗口仍待实测或进一步适配。暂不提供 macOS 版本。

## 校验与声明

Release 同时提供 `SHA256SUMS.txt`。可使用 `Get-FileHash .\WindowPet-0.0.1.exe -Algorithm SHA256` 校验下载文件。

本仓库用于发布程序和使用说明，核心源码不公开。第三方组件声明见 [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt)，也可在程序 About 中查看。
