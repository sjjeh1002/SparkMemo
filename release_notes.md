## SparkMemo v2.0.0 正式版（测试版）

### 更新内容

- **AI 助手升级为 DSH 风格 agent（借鉴 DeepSeek Harness 开源架构）**：
  - 原生 function calling 多轮循环：模型发起工具调用 → 应用真实执行 → 结果回填 → 继续，直到完成
  - AI 现在可以真正操作软件本身：添加/查询卡片、读取/修改设置、查询统计与计划、创建/查询笔记、直接跳转任意页面
  - 工具执行过程在会话中实时展示；失败明确说明，不编造结果
  - Android / Windows 双端支持；不依赖系统 Shell，安全可控
  - Anthropic(Claude) 等不支持原生工具的服务自动降级为纯文本问答
- 版本号更新为 v2.0.0（versionCode 6，测试版）

### 安装

- **Windows**：解压 `SparkMemo-Windows-x64-v2.0.0.zip`，双击 `smart_study.exe`（内置 OCR 组件，请勿删除 tesseract.exe / pdfium.dll / tessdata）
- **Android**：安装 `SparkMemo-Android-v2.0.0.apk`（Android 7.0+）；与旧版本冲突时请先卸载旧版再安装

### AI 配置（必需，AI 助手功能）

设置 → AI 模型配置 → 快速选择 DeepSeek / OpenAI / Kimi / GLM / Claude / Ollama → 填入 API Key → 测试连接。
AI 助手工具调用建议使用支持 function calling 的模型（DeepSeek / OpenAI / Kimi / GLM 均支持）。

### 文档

- 使用说明与产品优势见仓库 README
