<div align="center">

# Tufte-Style Typst Template

**优雅的学术教科书模板 | Elegant Academic Textbook Template**

[English](#english) | [中文](#中文)

[![GitHub](https://img.shields.io/github/license/exusiaiwei/template-typst-tufte)](https://github.com/exusiaiwei/template-typst-tufte/blob/main/LICENSE)
[![Typst](https://img.shields.io/badge/Typst-0.12.0+-239dad)](https://typst.app/)
[![GitHub stars](https://img.shields.io/github/stars/exusiaiwei/template-typst-tufte?style=social)](https://github.com/exusiaiwei/template-typst-tufte/stargazers)

<p align="center">
  <img src="https://img.shields.io/badge/Style-Tufte-blue" alt="Tufte Style"/>
  <img src="https://img.shields.io/badge/Layout-Wide_Margin-green" alt="Wide Margin"/>
  <img src="https://img.shields.io/badge/Feature-Sidenotes-orange" alt="Sidenotes"/>
</p>

</div>

---

## 中文

<div align="center">

### 追求恰到好处的高级感

*结构清晰 · 信息丰富 · 阅读舒适 · 克制优雅*

</div>

### ✨ 特性

<table>
<tr>
<td width="50%">

#### 📐 **Tufte 风格布局**
- 宽边栏设计，充分利用页面空间
- 优雅的边注系统
- 专业的学术排版

</td>
<td width="50%">

#### 🎨 **Obsidian 风格 Callout**
- 10 种预定义类型
- 彩色左侧边框
- 完美的视觉层次

</td>
</tr>
<tr>
<td width="50%">

#### 📊 **标准三线表**
- 顶部、表头下、底部三条粗线
- 自动表头加粗
- 符合学术规范

</td>
<td width="50%">

#### 🔢 **精致的边注**
- 上标样式编号
- 支持无编号边注
- 文献引用边注

</td>
</tr>
</table>

### 📦 快速开始

#### 1. 克隆仓库

```bash
git clone https://github.com/exusiaiwei/template-typst-tufte.git
cd template-typst-tufte
```

#### 2. 编译文档

```bash
typst compile main.typ
```

#### 3. 开始编写

编辑 `chapters/` 目录下的章节文件，或创建新章节：

```typst
#import "../template.typ": note, notecite, wideblock, callout

= 你的章节标题

这是正文内容#note[这是一个边注]。

#callout(type: "tip")[
  这是一个提示框！
]
```

### 🎯 核心功能

#### 边注系统

```typst
// 带编号的边注
正文内容#note[补充信息]

// 无编号边注
正文内容#note(numbered: false)[说明文字]

// 文献引用
研究表明#notecite(<key>)
```

#### Callout 块

```typst
#callout(type: "note")[这是笔记]
#callout(type: "tip")[这是提示]
#callout(type: "important")[这是重要信息]
#callout(type: "warning")[这是警告]
#callout(type: "example")[这是示例]
```

支持的类型：`note` 📝, `tip` 💡, `important` ⚠️, `warning` ⚡, `danger` 🔥, `success` ✅, `question` ❓, `example` 📌, `quote` 💬, `info` ℹ️

#### 三线表

```typst
#figure(
  table(
    columns: (2fr, 3fr, 3fr),
    table.header[列1][列2][列3],
    [数据1], [数据2], [数据3],
  ),
  caption: [表格标题]
)
```

#### 引用块

```typst
#quote(block: true, attribution: [作者名])[
  引用的内容...
]
```

### ⚙️ 配置

在 `main.typ` 中配置模板：

```typst
#show: tufte-textbook.with(
  title: "书名",
  subtitle: "副标题",
  authors: (
    (name: "作者", university: "机构", email: "邮箱"),
  ),
  date: datetime.today(),
  abstract: [...],

  // 可选：Logo
  logo: image("logo.png", width: 3cm),

  // 字体配置（可选，使用系统已安装的字体）
  font: ("Linux Libertine", "Source Han Serif SC", "Noto Serif CJK SC", "SimSun"),
  sansfont: ("Noto Sans", "Source Han Sans SC", "Noto Sans CJK SC", "SimHei"),
  codefont: ("JetBrains Mono", "Fira Code", "Cascadia Code", "Consolas"),
  fontsize: 10pt,

  // 样式配置
  theme-color: rgb("#1B255A"),
  lang: "zh",
  region: "cn",

  // 目录
  toc: true,
  toc-depth: 2,

  // 文献
  bibliography-file: "references.bib",
)
```

### 📁 项目结构

```
template-typst-tufte/
├── template.typ          # 核心模板文件
├── main.typ             # 主文档
├── chapters/            # 章节目录
│   ├── chapter01.typ
│   ├── chapter02.typ
│   └── chapter03.typ
├── references.bib       # 文献数据库
├── main.pdf            # 生成的 PDF
└── README.md           # 本文档
```

### 🎨 设计理念

- **简洁克制**：不过度装饰，保持学术风格
- **功能优先**：每个元素都有明确的功能目的
- **视觉层次**：通过颜色、粗细、间距建立清晰的层次
- **符合规范**：遵循中文学术排版标准

### 🔧 依赖

- Typst 0.12.0+
- `@preview/drafting:0.2.2` (自动安装)

推荐字体（可选，模板会自动回退）：
- **正文字体**: Linux Libertine, Source Han Serif SC, Noto Serif CJK SC
- **无衬线字体**: Noto Sans, Source Han Sans SC, Noto Sans CJK SC
- **代码字体**: JetBrains Mono, Fira Code, Cascadia Code, Consolas

💡 **提示**: 模板支持完全自定义字体，只需在配置中传入 `font`、`sansfont`、`codefont` 参数即可。

### 📄 许可证

本项目采用 [MIT 许可证](LICENSE)。

### 🙏 致谢

本模板灵感来源于：
- Edward Tufte 的排版设计理念
- [typst-orange-template](https://github.com/flavio20002/typst-orange-template)
- [tufte-memo](https://github.com/exusiaiwei/quarto-tufte-memo) Quarto 模板

### 📮 反馈

如有问题或建议，欢迎：
- 提交 [Issue](https://github.com/exusiaiwei/template-typst-tufte/issues)
- 发起 [Pull Request](https://github.com/exusiaiwei/template-typst-tufte/pulls)
- 联系作者：[@exusiaiwei](https://github.com/exusiaiwei)

---

## English

<div align="center">

### Pursuing Just-Right Sophistication

*Clear Structure · Rich Information · Comfortable Reading · Elegant Restraint*

</div>

### ✨ Features

<table>
<tr>
<td width="50%">

#### 📐 **Tufte-Style Layout**
- Wide margin design
- Elegant sidenote system
- Professional academic typesetting

</td>
<td width="50%">

#### 🎨 **Obsidian-Style Callouts**
- 10 predefined types
- Colorful left border
- Perfect visual hierarchy

</td>
</tr>
<tr>
<td width="50%">

#### 📊 **Standard Three-Line Tables**
- Three thick lines (top, header, bottom)
- Auto-bold headers
- Academic standard compliant

</td>
<td width="50%">

#### 🔢 **Refined Sidenotes**
- Superscript-style numbering
- Unnumbered notes support
- Citation sidenotes

</td>
</tr>
</table>

### 📦 Quick Start

#### 1. Clone Repository

```bash
git clone https://github.com/exusiaiwei/template-typst-tufte.git
cd template-typst-tufte
```

#### 2. Compile

```bash
typst compile main.typ
```

#### 3. Start Writing

Edit chapter files in `chapters/` or create new ones:

```typst
#import "../template.typ": note, notecite, wideblock, callout

= Your Chapter Title

This is main text#note[This is a sidenote].

#callout(type: "tip")[
  This is a tip callout!
]
```

### 🎯 Core Features

#### Sidenote System

```typst
// Numbered sidenote
Main text#note[Supplementary info]

// Unnumbered sidenote
Main text#note(numbered: false)[Description]

// Citation
Research shows#notecite(<key>)
```

#### Callout Blocks

```typst
#callout(type: "note")[This is a note]
#callout(type: "tip")[This is a tip]
#callout(type: "important")[This is important]
#callout(type: "warning")[This is a warning]
#callout(type: "example")[This is an example]
```

Supported types: `note` 📝, `tip` 💡, `important` ⚠️, `warning` ⚡, `danger` 🔥, `success` ✅, `question` ❓, `example` 📌, `quote` 💬, `info` ℹ️

#### Three-Line Tables

```typst
#figure(
  table(
    columns: (2fr, 3fr, 3fr),
    table.header[Col1][Col2][Col3],
    [Data1], [Data2], [Data3],
  ),
  caption: [Table Caption]
)
```

#### Quote Blocks

```typst
#quote(block: true, attribution: [Author])[
  Quote content...
]
```

### ⚙️ Configuration

Configure the template in `main.typ`:

```typst
#show: tufte-textbook.with(
  title: "Book Title",
  subtitle: "Subtitle",
  authors: (
    (name: "Author", university: "Institution", email: "email"),
  ),
  date: datetime.today(),
  abstract: [...],

  // Optional: Logo
  logo: image("logo.png", width: 3cm),

  // Font configuration (optional, uses system-installed fonts)
  font: ("Linux Libertine", "Source Han Serif SC", "Noto Serif CJK SC", "SimSun"),
  sansfont: ("Noto Sans", "Source Han Sans SC", "Noto Sans CJK SC", "SimHei"),
  codefont: ("JetBrains Mono", "Fira Code", "Cascadia Code", "Consolas"),
  fontsize: 10pt,

  // Style
  theme-color: rgb("#1B255A"),
  lang: "en",
  region: "us",

  // TOC
  toc: true,
  toc-depth: 2,

  // Bibliography
  bibliography-file: "references.bib",
)
```

### 📁 Project Structure

```
template-typst-tufte/
├── template.typ          # Core template
├── main.typ             # Main document
├── chapters/            # Chapter directory
│   ├── chapter01.typ
│   ├── chapter02.typ
│   └── chapter03.typ
├── references.bib       # Bibliography
├── main.pdf            # Generated PDF
└── README.md           # This file
```

### 🎨 Design Philosophy

- **Elegant Restraint**: No excessive decoration
- **Function First**: Every element serves a purpose
- **Visual Hierarchy**: Clear layers through color, weight, and spacing
- **Standards Compliant**: Following academic typesetting conventions

### 🔧 Dependencies

- Typst 0.12.0+
- `@preview/drafting:0.2.2` (auto-installed)

Recommended fonts (optional, template will auto-fallback):
- **Serif fonts**: Linux Libertine, Source Han Serif SC, Noto Serif CJK SC
- **Sans-serif fonts**: Noto Sans, Source Han Sans SC, Noto Sans CJK SC
- **Monospace fonts**: JetBrains Mono, Fira Code, Cascadia Code, Consolas

💡 **Tip**: Template supports full font customization via `font`, `sansfont`, and `codefont` parameters.

### 📄 License

This project is licensed under the [MIT License](LICENSE).

### 🙏 Acknowledgments

Inspired by:
- Edward Tufte's typographic design principles
- [typst-orange-template](https://github.com/flavio20002/typst-orange-template)
- [tufte-memo](https://github.com/exusiaiwei/quarto-tufte-memo) Quarto template

### 📮 Feedback

Issues and suggestions are welcome:
- Submit an [Issue](https://github.com/exusiaiwei/template-typst-tufte/issues)
- Open a [Pull Request](https://github.com/exusiaiwei/template-typst-tufte/pulls)
- Contact: [@exusiaiwei](https://github.com/exusiaiwei)

---

<div align="center">

**Made with ❤️ for the academic community**

⭐ Star this repo if you find it helpful!

</div>
