## SparkMemo v1.2.1 正式版

### 更新内容

- **PDF 提取引擎升级为开源 pdfium(pdfrx)**:
  - 此前 Android 端对无 ToUnicode 映射的中文 PDF 提取为空(只有页码),Syncfusion 商业库无能为力
  - 现升级为 pdfium 引擎二次提取(开源,Chrome/Edge 同款内核),提取率远超商业库,此类 PDF 可直接导入
  - 提取仍为空时自动进入 OCR(Android ML Kit 中文 / Windows Tesseract)
- 版本号更新为 v1.2.1(versionCode 5)

### 安装

- **Windows**:解压 `SparkMemo-Windows-x64-v1.2.1.zip`,双击 `smart_study.exe`(内置 OCR 组件,请勿删除 tesseract.exe / pdfium.dll / tessdata)
- **Android**:安装 `SparkMemo-Android-v1.2.1.apk`(Android 7.0+);与旧版本冲突时请先卸载旧版再安装

### AI 配置(可选)

设置 → AI 模型配置 → 快速选择 DeepSeek / OpenAI / Kimi / GLM / Claude / Ollama → 填入 API Key → 测试连接。
不配置 AI 也可使用全部本地功能。

### 文档

- 使用说明与产品优势见仓库 README
