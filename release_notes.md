## SparkMemo v2.2.0 正式版（测试版）

### 更新内容

- **AI 自动反思（新机制）**：设置开关恢复，改为**应用启动时**检查——距上次自动反思超过一天（跨天）即自动生成今日反思草稿；成功记录 `reflect.last_auto_at`，失败下次启动重试
- **AI 反思不填写专注度 / 情绪**：AI 生成的反思草稿与记录中专注 / 情绪为「未填写」（数据库 NULL，不是 0），**不参与 AI 计划编排**；反思编辑器仅在用户主动调整后才写入数值
- **AI 计划定时化**：「AI 辅助编排计划」开启后，除复习会话结束触发外，**应用启动时**距上次自动调整超过一天即自动执行（AI 依据本周反思内容 + 卡片知识点分布调整本周计划），记录 `plan.last_auto_at`
- **AI 应用内数据修改**能力保留：16 个工具，可读取全部应用数据并动态修改卡片 / 笔记 / 反思 / 计划 / 设置
- 版本号更新为 v2.2.0（versionCode 8）

### 安装

- **Windows**：解压 `SparkMemo-Windows-x64-v2.2.0.zip`，双击 `smart_study.exe`（内置 OCR 组件，请勿删除 tesseract.exe / pdfium.dll / tessdata）
- **Android**：安装 `SparkMemo-Android-v2.2.0.apk`（Android 7.0+）；与旧版本冲突时请先卸载旧版再安装

### AI 配置

设置 → AI 模型配置 → 快速选择 DeepSeek / OpenAI / Kimi / GLM / Claude / Ollama → 填入 API Key → 测试连接。
AI 助手工具调用建议使用支持 function calling 的模型（DeepSeek / OpenAI / Kimi / GLM 均支持）。

### 文档

- 使用说明与产品优势见仓库 README
