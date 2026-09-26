# v2.5.1 交付与验证

2026-09-26。应用 **2.5.1+21**，数据库 **v9**。改动、测试用例和边界详见 [开发记录](DEVELOPMENT_v2.5.1.md)。

## 已验证

- 全量测试 **573 通过、3 手动项默认跳过**；静态检查 **0 error、11 warning、136 info**。
- 实际库副本迁移测试单独通过；桌面程序更新后实际库也已升至 v9，98 卡、1 笔记、85 知识点、1 复习日志、1 作答记录的全部旧列与升级前备份逐行一致，integrity_check=ok。
- 旧版程序备份：`deliverables/smart_study-windows-x64.pre-v2.5.1`；数据库备份：`AppData/Roaming/com.smartstudy/smart_study/study_app.db.pre-v2.5.1.bak`。未删除先前备份及离线资源。
- 桌面 `SparkMemo.lnk` 原目标目录已更新。进程启动、响应及数据库升级检查通过，不声称全部功能已人工 GUI 验收；验证专用隐藏进程已结束。
- Windows/Android 公开候选、开发版共四种构建成功。143 个 lib/test 文件与原项目、四个构建目录、开发包源码及私有上传暂存逐项哈希一致。
- 公开 Windows 包不含源码，含 Tesseract/tessdata/PDFium；Android 经 FixApk.java、16 KB zipalign、v2/v3 签名，15 个原生库及 resources.arsc 均 STORED，CRC 正确，无重复条目或 lib/lib 前缀；versionCode=21、minSdk=24。
- v2.5.0 真实长文已保存结果在新代码下恢复回放通过，0 新 API 请求；本轮没有把它算作新一轮联网生成验收。
- Android 16 真机加固包覆盖安装成功，版本 2.5.1/code 21；从未运行状态冷启动成功（927ms），主页可见、进程存活且未发现关键异常。未卸载或清除应用数据；没有据此宣称手机数据库已逐字段比对。

## SHA-256

| 包 | SHA-256 |
|---|---|
| SparkMemo-Public-Windows-x64-v2.5.1.zip | 50d735693c355546cd9c1790788a0ebe451279e90ab7ef8ac9d8e10e4acedcac |
| SparkMemo-Public-Android-v2.5.1.apk | 0ec98cca3eac767fe98be4b934a297317733c2a097dbc8ca187f4eb0c42c4b48 |
| SparkMemo-Development-Windows-x64-v2.5.1.zip | 9024b94bcd79c99f066d47bd16bef5f69f4cfdb20580271de7a005ff8c1a7bb1 |
| SparkMemo-Development-Android-v2.5.1.apk | 2212501fce026f61c67bc1870a7a849422a3eec386bdb249751a909f8ece27d7 |

## 分发与剩余工作

- 本地开发版：桌面 `SparkMemo开发版/v2.5.1`，含 Source、Windows、Android。源码和未加固包只允许进入 PRIVATE 仓库。
- 私有发布条目：[v2.5.1-dev](https://github.com/sjjeh1002/SparkMemo-Development/releases/tag/v2.5.1-dev)。是否完成上传以 GitHub 条目实际状态及本地发布核验回执为准。
- 本地内测、固定正式版、公开版目录使用新 Windows ZIP；APK 放在 `Android已验证启动`。此前 `Android待真机验证` 中本版候选已移至该目录，其余版本保留原验收状态。已验证单台 Android 16 安装/冷启动，系统输入法等完整交互仍未真机验收。
- 公开版发布条目：[v2.5.1](https://github.com/sjjeh1002/SparkMemo/releases/tag/v2.5.1)，只附运行包，不上传最新开发源码或调试符号。
- 本轮只完成草稿浏览/导入的分批读取，生成核心的磁盘流式续跑仍未完成；旧 settings 整块草稿转换及单个特大分段的内存峰值仍需继续优化。
- 仍有语义覆盖、跨来源数据库整数 ID 合并及完整人工 GUI 验收风险；不宣称全部任务已完成或没有算法问题。
