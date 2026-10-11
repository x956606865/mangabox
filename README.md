<p align="center">
  <img src="docs/assets/icon.png" width="128" alt="MangaBox 图标">
</p>

<h1 align="center">MangaBox 漫画成书</h1>

<p align="center">
  把一个装着漫画图片的文件夹，做成适合电子书阅读器的 EPUB / CBZ。<br>
  自动拆页、裁掉白边、放大到阅读器分辨率并居中。免费，双击就能用。
</p>

<p align="center">
  <a href="https://github.com/x956606865/mangabox/releases/latest"><b>下载最新版</b></a> ·
  <a href="https://mangabox.moukeer.com/">官网</a> ·
  <a href="https://github.com/x956606865/mangabox/issues/new/choose">反馈问题</a>
</p>

<p align="center">
  <img src="docs/assets/screenshots/04-confirm.png" width="860" alt="确认书名与阅读器">
</p>

## 能做什么

- **自动拆页**：左右两页拼在一起的横图会自动拆开；日漫先右后左，国漫、韩漫、欧美漫画可以选从左往右。
- **裁掉白边**：模型找出每页正文（包括出框的人物、对话框和拟声字）的范围，页码和外围水印不会影响裁切。
- **放大与居中**：用 MangaJaNai 放大模型把画面放大到阅读器分辨率，全书统一大小，翻页时不会忽大忽小。
- **先预览，再检查**：做好后按阅读器屏幕的样子翻看；模型不太确定的页排在前面，拖动红框调整（可以放大、撤销），一键重新制作。
- **整套制作**：一个文件夹里按卷分好的多卷漫画（每卷一个子文件夹或一个压缩包），确认卷号后每卷做成一本，系列名和卷号写进电子书；中途停下也能接着做。
- **扫描件画质修正**：纸面发黄、发灰的页自动拉白，歪了的页自动拉正；每页先检测再决定做不做，正常的数字版漫画不会被改动。
- **去水印**：每页同一位置的半透明网站水印（logo、网址）可以去掉，看过去除前后的对比再确认。
- **为墨水屏优化**：可选锐化和 16 级灰抖动，附带设备测试页，在阅读器上对比后再决定。
- **直接打开压缩包**：支持 zip / cbz / rar / 7z，把文件夹或压缩包拖进窗口就能开始。
- **书架**：整套叠成一套、每个阅读器一个版本；一键给另一台阅读器重做整套，或直接复制到插在电脑上的阅读器。
- **安全**：原图不会被修改，也不会上传到网络。

支持的阅读器：BOOX Leaf 5 / Tab Mini C / Tab Ultra C / Tab X C，Kindle / Paperwhite / Colorsoft / Scribe，Kobo Clara / Libra / Sage / Elipsa 2E；其他阅读器可以自定义屏幕分辨率。

## 截图

| 开始 | 制作中 |
| --- | --- |
| ![开始](docs/assets/screenshots/01-start.png) | ![制作中](docs/assets/screenshots/05-working.png) |
| **做好了** | **检查并修正** |
| ![完成](docs/assets/screenshots/06-done.png) | ![检查并修正](docs/assets/screenshots/08-review.png) |
| **整套制作** | **书架（深色模式）** |
| ![整套制作](docs/assets/screenshots/03-series-dialog.png) | ![书架](docs/assets/screenshots/10-library-dark.png) |

截图中的漫画是程序生成的示意图。

## 下载与安装

到 [Releases](https://github.com/x956606865/mangabox/releases/latest) 下载对应系统的安装包：

| 系统 | 文件 | 要求 |
| --- | --- | --- |
| macOS | `MangaBox-版本-macos-arm64.dmg` | Apple 芯片（M1 及更新），macOS 12 以上 |
| Windows | `MangaBox-版本-windows-x64.zip` | 64 位 Windows 10 / 11 |

### macOS 第一次打开

MangaBox 是免费软件，没有向苹果付费做“公证”，第一次打开时系统会提示无法验证开发者：

1. 打开 dmg，把 MangaBox 拖到“应用程序”。
2. 双击 MangaBox，看到提示后点“完成”。
3. 打开“系统设置 → 隐私与安全性”，在页面下方点“仍要打开”，输入密码确认。

以后就可以像普通软件一样直接打开。

### Windows

1. 右键 zip →“全部解压缩”（不要在压缩包里直接运行）。
2. 打开解压出的 MangaBox 文件夹，双击“启动 MangaBox.bat”。
3. 如果出现“Windows 已保护你的电脑”，点“更多信息”→“仍要运行”。

macOS 用 Apple 芯片加速；Windows 有显卡（NVIDIA / AMD / Intel）时自动用显卡加速，不需要另外下载，用不了时改用 CPU（慢一些，效果一样）。

## 常见问题

**会上传我的漫画吗？** 不会。所有处理都在你的电脑上完成。联网只用于检查新版本（可在设置里关闭）。

**做好的书在哪里？** macOS 在“文稿/MangaBox”，Windows 在“文档\MangaBox”，也可以在“设置”里一键打开。

**支持压缩包吗？** 支持 zip / cbz / rar / 7z，可以直接选择或拖进窗口；有密码的压缩包需要先解压。

**怎么更新？** 有新版本时 MangaBox 会提示，在“设置 → 关于”点“更新并重启”，会自动下载、安装并重新打开（0.5.0 起）。

**遇到问题？** 请到 [Issues](https://github.com/x956606865/mangabox/issues/new/choose) 反馈，最好附上诊断信息：在“设置 → 遇到问题”点“导出诊断信息”，会在“下载”文件夹生成一个压缩包（不含漫画图片）。

## 许可与致谢

MangaBox 免费提供，本仓库用于发布安装包和收集反馈。

随安装包附带的放大模型 [MangaJaNai / IllustrationJaNai](https://github.com/the-database/MangaJaNai)（作者 the-database）采用 **CC BY-NC 4.0**，只能用于非商业用途。其他开源组件的许可见安装包内的《第三方许可》。
