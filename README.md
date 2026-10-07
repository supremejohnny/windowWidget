# Window Pet

把小挂件挂在打开的窗口上，让绳子与角色随着窗口移动自然摆动喵

## 下载

| 平台 | 下载 | Release |
| --- | --- | --- |
| macOS · Apple Silicon | [WindowPet-0.0.4-macos-arm64.zip](https://github.com/supremejohnny/windowWidget/releases/download/v0.0.4/WindowPet-0.0.4-macos-arm64.zip) | [macOS v0.0.4](https://github.com/supremejohnny/windowWidget/releases/tag/v0.0.4) |
| Windows | [WindowPet-0.0.1.exe](https://github.com/supremejohnny/windowWidget/releases/download/v0.0.1/WindowPet-0.0.1.exe) | [Windows v0.0.1](https://github.com/supremejohnny/windowWidget/releases/tag/v0.0.1) |

macOS 包要求 Apple Silicon（M 系列芯片）与 macOS 12 及以上，不适用于 Intel Mac；Windows 为单个 EXE，无需额外资源文件夹喵

## macOS 使用

1. 解压 ZIP，将 `Window Pet.app` 拖入“应用程序”，双击打开。
2. 首次下载版本使用临时签名，尚未经过 Apple 公证。若提示无法验证开发者，确认下载来源与校验值后，可按 [Apple 的打开说明](https://support.apple.com/en-us/102445)，在尝试启动后前往“系统设置 → 隐私与安全性 → 仍要打开”；较旧系统名称可能不同。
3. 点击“演示窗口”可直接体验。挂到其他应用时，选择应用、角色、角落与绳长，点击“挂载”，然后切到该应用要挂的窗口，自动完成绑定；每个应用只列一次，无需猜窗口编号。
4. 点击角色戳动；点击锚点收起或展开；关闭控制面板退出。

无需浏览器、Electron 或额外 Swift 运行环境。演示窗口不需要辅助功能授权；控制面板中的“辅助功能设置”可帮助配置其他应用的事件跟随，未授权时仍有屏幕帧采样。应用不会自行修改系统权限喵

macOS v0.0.4 使用 10 段动态绳，保留绳身弯曲、回弹和挂件旋转；小幅窗口移动经过滤波，避免上段幅度过大。已验证 Apple Silicon 本机的微动、慢拖、甩动、戳动、收起/展开、普通遮挡和透明点击穿透。台前调度开启时，已用独立应用验证应用切换、最小化恢复、全屏进出与同应用多窗口焦点；多屏、不同应用侧边缩略图点击与长期占用仍需继续实测喵

应用列表包括后台和其他桌面的正常桌面应用，并过滤内部与系统辅助窗口。挂件只在绑定窗口进入前台时显示，切换到后台会暂停并释放点击，返回后自动恢复；切换期间冻结动态，恢复后继续摆动。前台挂件使用浮动层级，应用移动时把自己的普通窗口置前也不会盖住挂件。后台挂件暂不显示是当前设计；重新挂载可绑定同应用的另一个窗口。台前调度适配要求 macOS 13 及以上喵

## Windows 使用

1. 双击 EXE，选择要挂载的窗口和挂件。
2. 选择左上 / 右上 / 左下 / 右下，以及短 / 中 / 长 / 超长绳子。
3. 点击 **Attach** 开始挂载。
4. 点击挂件戳动；点击锚点收起或展开。
5. **Detach** 解除挂载；关闭设置窗口退出。

面向 Windows 10 / 11，使用系统 .NET Framework；完整验证环境为 Windows 10 22H2 x64，Windows 11、ARM64、混合 DPI 多屏和特殊窗口仍待实测。Windows 本机观察私有工作集约 14 MiB，用户反馈约 2.5 小时运行正常、无卡顿；这些不是 macOS 占用数据，实际占用随环境变化喵

## 校验与声明

每个 Release 都提供自己的 `SHA256SUMS.txt`。macOS 可使用 `shasum -a 256 WindowPet-0.0.4-macos-arm64.zip`，Windows 可使用 `Get-FileHash .\WindowPet-0.0.1.exe -Algorithm SHA256` 校验喵

本仓库仅发布程序和使用说明，核心源码不公开。第三方组件与角色权利说明见 [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt)，macOS 包内也附带第三方说明与 MIT 许可证。`amiya_test1` 是用户提供的测试角色，角色权利属于原权利人，不属于物理组件的 MIT 授权喵
