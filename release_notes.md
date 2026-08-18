## SparkMemo v1.1.0 正式版

### 更新内容

- **修复 PDF 导入闪退**:全链路异常防护,解析失败给出明确提示而不再崩溃(Android 低内存设备 OOM 防护:超过 80MB / 500 页直接拒绝并提示)
- **修复 PDF 导入内容错乱**:提取为空时明确提示「未提取到文本(可能为扫描件/图片型 PDF,或字体无文本映射)」,不再静默产出"只有页码"的无效内容;单页失败不中断整篇
- 版本号更新为 v1.1.0(versionCode 3)

### 安装

- **Windows**:解压 `SparkMemo-Windows-x64-v1.1.0.zip`,双击 `smart_study.exe`
- **Android**:安装 `SparkMemo-Android-v1.1.0.apk`(Android 7.0+);与旧版本冲突时请先卸载旧版再安装

### AI 配置(可选)

设置 → AI 模型配置 → 快速选择 DeepSeek / OpenAI / Kimi / GLM / Claude / Ollama → 填入 API Key → 测试连接。
不配置 AI 也可使用全部本地功能。

### 文档

- 使用说明与产品优势见仓库 README
