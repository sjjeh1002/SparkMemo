## SparkMemo v2.1.0 正式版（测试版）

### 更新内容

- **AI 权限扩大（读全部数据 + 动态修改）**：新增 7 个工具，工具总数 16——
  - `get_all_data`：读取应用全部自身数据（设置 / 卡片与标签分布 / 笔记 / 反思 / 计划 / 复习统计 / 成就 / 插件）
  - `update_card` / `delete_card`：按问题或 id 定位修改、删除卡片
  - `update_note` / `delete_note`：按标题修改、删除笔记（删除连同其卡片）
  - `save_reflection`：保存 / 更新某日反思记录
  - `update_plan`：设置 / 修改某日计划
- **移除 AI 自动反思与 AI 自动计划**：不再默认自动触发（反思页手动「AI 反思」、计划页手动「AI 调整本周」保留）
- **任务编排默认 FSRS 算法**：「AI 辅助编排计划」改为设置中手动开启（默认关）；开启后复习结束，AI 根据**本周反思内容 + 卡片知识点分布**调整本周计划
- **复习策略按 FSRS 官方规范核对**（[fsrs4anki wiki](https://github.com/open-spaced-repetition/fsrs4anki/wiki)）：FSRS-5 21 参数默认值、retention=0.9、Again/Hard/Good/Easy 四档映射、遗忘曲线 R(t) 与状态机（New→Learning→Review、Again→Relearning）全部与官方一致
- 版本号更新为 v2.1.0（versionCode 7）

### 安装

- **Windows**：解压 `SparkMemo-Windows-x64-v2.1.0.zip`，双击 `smart_study.exe`（内置 OCR 组件，请勿删除 tesseract.exe / pdfium.dll / tessdata）
- **Android**：安装 `SparkMemo-Android-v2.1.0.apk`（Android 7.0+）；与旧版本冲突时请先卸载旧版再安装

### AI 配置

设置 → AI 模型配置 → 快速选择 DeepSeek / OpenAI / Kimi / GLM / Claude / Ollama → 填入 API Key → 测试连接。
AI 助手工具调用建议使用支持 function calling 的模型（DeepSeek / OpenAI / Kimi / GLM 均支持）。

### 文档

- 使用说明与产品优势见仓库 README
