# 公开版与开发版分发约定

2026-10-08 起仅开发、验收和发布 Android，保留 Flutter / Dart。Windows 包及说明属于历史，后续构建和打包仅输出 Android。见 [Android 支持范围](ANDROID_SUPPORT.md)。


- **公开版（Public）**：加固的 Windows/Android 运行包，不附带应用源码和调试符号；发布到 GitHub Releases。文件名必须含 `Public`，Release 标题写「公开版」。预发布/待真机验证是验收状态，不是另一种版本类型。
- **开发版（Development）**：未加固的程序与对应源码、测试、脚本，在本机和经验证为 PRIVATE 的 `sjjeh1002/SparkMemo-Development` 仓库保存；可以上传该私有仓库的 Releases，禁止上传公开仓库。文件名含 `Development`；Windows 不传 `--obfuscate`，Android 同时关闭 R8，且不运行手工 strip/FixApk 加固流程。正常 Release AOT 编译和 APK 签名仍保留，不等于 Debug 模式。

本机目录：桌面 `SparkMemo公开版` 与 `SparkMemo开发版`。原 `SparkMemo内测版` 固定目录保留为兼容入口，说明指向新分类。`SparkMemo.lnk` 仍指向项目 deliverables 的公开版程序目录，正式版 v2.2.1 不覆盖。

开发版与公开版目前使用相同应用 ID/数据目录，不应并行运行，不保证可同时安装；切换前备份数据。Android 两类包都必须明确记录真机安装验证状态，不能以构建/签名通过代替安装验收。

构建：公开版用 `tools/Build-LearningMvp.ps1` 和 `tools/Harden-LearningMvp.ps1`；开发版用 `tools/Build-Development.ps1`。公开版构建显式关闭开发 Gradle 开关，防止误发未加固包。

公开仓库 `sjjeh1002/SparkMemo` 仍为 PUBLIC，其已有代码及 GitHub 自动 Source code 归档仍可见，不擅自修改历史。2026-09-18 按用户要求新建 PRIVATE 开发仓库并上传 v2.3.2 基线，后续开发源代码只推送私有仓库。上传前后均验证 visibility；不提交用户数据库、密钥、登录凭据、签名私钥、日志或构建缓存。
