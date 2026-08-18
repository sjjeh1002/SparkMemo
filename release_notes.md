## SparkMemo v1.2.0 正式版

### 更新内容

- **内置 OCR(双平台)**:
  - 扫描件 / 图片型 PDF 现在会自动识别文字:PDF 无文本层时自动逐页渲染 → OCR → 导入笔记
  - Android:Google ML Kit 中文文本识别(模型随包,完全离线,印刷体精度高)
  - Windows:随包内置 Tesseract 5.4 + 中文语言包(chi_sim+eng,离线)
- PDF 导入全链路异常防护,超大文件 / 超多页数限制
- 版本号更新为 v1.2.0(versionCode 4)

> 说明:OCR 针对印刷体扫描件效果最佳;手写内容识别率有限。Windows 安装包因内置 OCR 引擎体积增大属正常。

### 安装

- **Windows**:解压 `SparkMemo-Windows-x64-v1.2.0.zip`,双击 `smart_study.exe`(内置 OCR 组件,解压后请勿单独删除 tesseract.exe / pdfium.dll / tessdata 目录)
- **Android**:安装 `SparkMemo-Android-v1.2.0.apk`(Android 7.0+);与旧版本冲突时请先卸载旧版再安装

### AI 配置(可选)

设置 → AI 模型配置 → 快速选择 DeepSeek / OpenAI / Kimi / GLM / Claude / Ollama → 填入 API Key → 测试连接。
不配置 AI 也可使用全部本地功能。

### 文档

- 使用说明与产品优势见仓库 README
