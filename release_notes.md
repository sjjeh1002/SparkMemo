## SparkMemo v1.0.1 正式版

### 更新内容

- **修复 Android 网络功能**:补齐 `INTERNET` 权限(此前 release 包缺少该权限,导致「获取模型 / 测试连接 / AI 调用 / 局域网同步」全部失败)
- **新增存储访问授权弹窗**:首次启动说明用途(笔记导入 / 背景图 / 数据备份)→ 请求系统权限;拒绝后引导至系统设置开启;仅首次自动询问,已授权不再打扰
- 版本号更新为 v1.0.1(versionCode 2)

### 安装

- **Windows**:解压 `SparkMemo-Windows-x64-v1.0.1.zip`,双击 `smart_study.exe`
- **Android**:安装 `SparkMemo-Android-v1.0.1.apk`(Android 7.0+);与旧版本冲突时请先卸载旧版再安装

### AI 配置(可选)

设置 → AI 模型配置 → 快速选择 DeepSeek / OpenAI / Kimi / GLM / Claude / Ollama → 填入 API Key → 测试连接。
不配置 AI 也可使用全部本地功能。

### 文档

- 使用说明与产品优势见仓库 README
