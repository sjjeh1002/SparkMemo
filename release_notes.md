## SmartMemo v1.0.0 正式版

智能记忆学习助手:FSRS-5 间隔重复算法 + AI 全链路(制卡 / 出题 / 反思 / 计划 / 助手 / 定制),本地优先,Windows + Android 双平台。

### 更新内容

- AI 制卡 / 出题**不设数量上限**:内容驱动、多轮并行、失败自动重试
- AI 生成卡片可导入到**已有 / 新建卡片组**
- 计划驱动新卡,新卡完成数真实累计,每日限额按日递减
- 修复:复习完成页「再来一轮」崩溃、同步基线退化、同步页初始化健壮性
- 设置页每日新卡上限交互重构(滑块 5–1000 + 输入框 1–99999999 + 一键不限)
- 统计 / 反思页实时刷新;周度 AI 分析持久化
- 安全加固:Release AOT + Dart 符号混淆 + Android R8 + DWARF 剥离 + 构建路径脱敏

### 安装

- **Windows**:解压 `SmartMemo-Windows-x64-v1.0.0.zip`,双击 `smart_study.exe`
- **Android**:安装 `SmartMemo-Android-v1.0.0.apk`(Android 7.0+);与旧版冲突时请先卸载旧版

### AI 配置(可选)

设置 → AI 模型配置 → 快速选择 DeepSeek / OpenAI / Kimi / GLM / Claude / Ollama → 填入 API Key → 测试连接。
不配置 AI 也可使用全部本地功能。

### 文档

- 使用说明与产品优势见仓库 README
