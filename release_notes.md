## SparkMemo v2.2.2 测试版

### 更新内容

- **AI 反思草稿防丢失**：草稿跨天未处理时，下次自动反思 / 手动 AI 反思前会**先自动保存为当天正式反思记录**，再生成新草稿（目标日期已有记录则不重复保存）；应用 / 丢弃草稿后同步清除记录
- **卡片库标签多选**：可同时勾选多个卡组筛选卡片（含任一勾选标签即显示）；「自己制作卡片」时新卡标签自动填入**全部勾选**的卡组（去重、卡组在前，保存后提示归入结果）
- 版本号更新为 v2.2.2（versionCode 10）

### 安装

- **Windows**：解压 `SparkMemo-Windows-x64-v2.2.2.zip`，双击 `smart_study.exe`（内置 OCR 组件，请勿删除 tesseract.exe / pdfium.dll / tessdata）
- **Android**：安装 `SparkMemo-Android-v2.2.2.apk`（Android 7.0+）；与旧版本冲突时请先卸载旧版再安装

### 文档

- 使用说明与产品优势见仓库 README
