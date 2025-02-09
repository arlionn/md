# VScode 插件：安装、配置和使用

&emsp; 

> [ChatGPT 提示词](https://chatgpt.com/share/671fa55c-ea48-8005-a126-97b9ee5c5d13)

&emsp; 

## VScode 简介

Visual Studio Code (简称 VScode) 是由微软开发的一款开源、免费且功能强大的代码编辑器。它轻量、跨平台，支持 Windows、macOS 和 Linux 系统。VScode 的核心优势在于其高度可扩展的插件系统，用户可以通过安装各种插件来定制编辑器的功能，适应不同的编程语言和工作场景。

- [VScode 下载](https://code.visualstudio.com/)


## 什么是 VScode 插件？

VScode 插件是由第三方开发者或微软官方提供的功能扩展模块。它们能够增强 VScode 的功能，实现新的编程语言支持、UI 改进、自动化任务等。插件安装、更新和管理都可以通过 VScode 内置的插件市场轻松完成。通过合理的插件组合，用户可以打造一个完全满足个人需求的开发环境。

## 插件的使用

![20241028114241](https://fig-lianxh.oss-cn-shenzhen.aliyuncs.com/20241028114241.png)

### 搜索插件

VScode 内置了一个方便的插件市场，用户可以轻松搜索并安装插件，步骤如下：
  1. 点击左侧栏的 **Extensions（扩展）** 图标，或使用快捷键 `Ctrl+Shift+X` 打开插件市场；
  2. 在顶部的搜索框输入插件名称或关键词（如 "Python"、"Markdown"、"Git"）；
  3. VScode 会展示相关插件的搜索结果。

对于出现的多个备选插件，建议优先选择 **star 数较多**、**评分高** 且 **更新频率高** 的插件。这些插件通常经过大量用户的验证，功能较为稳定。可以点击插件名称查看详细描述、用户评价和更新历史，综合这些因素选择最适合的插件。

### 安装插件

安装插件非常简单：
  1. 找到需要的插件后，点击 **Install（安装）** 按钮；
  2. 安装完成后插件会自动启用，无需重启编辑器。

插件安装后，通常会弹出一个简短的欢迎页面，向你介绍插件的基本功能和使用方法。

### 插件管理与使用

插件安装后可以立即使用，但用户还可以根据需要对插件进行管理和配置：
  
- **启用与禁用插件**：所有安装的插件都会默认启用。若暂时不需要某个插件，可以点击插件列表中的齿轮图标，选择 **Disable（禁用）**。禁用的插件不会影响系统性能，但保留在系统中，方便日后重新启用。
  
- **快捷键管理**：许多插件带有默认的快捷键。通过 **File > Preferences > Keyboard Shortcuts** 菜单，用户可以查看和自定义插件的快捷键。如果遇到快捷键冲突，用户可以禁用冲突的快捷键或为不同插件功能分配新的快捷键。
  
- **插件冲突**：如果多个插件提供了类似功能，可能会发生冲突。通过插件管理界面可以查看当前启用的插件，禁用多余插件以避免冲突和性能下降。特别是对于大项目或多语言支持时，谨慎选择相同功能的插件尤为重要。
  
- **查看生效的插件**：在插件管理界面，你可以查看当前启用的所有插件。当插件过多导致编辑器运行缓慢时，禁用不必要的插件可以显著提升性能。

## 常用插件推荐

本节将介绍 VScode 中常用的插件，涵盖代码编写、文档处理、思维导图、幻灯片制作等多个方面，帮助你进一步扩展 VScode 的功能。

### Markdown 插件

Markdown 是轻量级的标记语言，广泛应用于技术文档、博客写作等场景。以下是几款常用的 Markdown 插件：

- **Markdown All in One**：[安装链接](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)：支持 Markdown 的实时预览、格式化、目录生成等功能，非常适合编写长篇文档。
- **Markdown Preview Enhanced**：[安装链接](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced)：增强版 Markdown 预览插件，支持导出 PDF、插入图表、流程图等功能。
- **MarkdownLint**：[安装链接](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)：提供 Markdown 格式规范检查，帮助用户保持文档格式一致性。

### R 插件

VScode 支持多种编程语言，通过以下插件可以增强 VScode 对 R 语言的支持，尤其适合数据分析和统计工作流：

- **R Language Support**：[安装链接](https://marketplace.visualstudio.com/items?itemName=Ikuyadeu.r)：这是 VScode 官方提供的 R 插件，支持 R 语言的语法高亮、代码自动补全以及片段执行等功能，还集成了 R 终端，帮助用户直接在 VScode 中运行 R 代码。
- **R Tools**：[安装链接](https://marketplace.visualstudio.com/items?itemName=Mikhail-Arkhipov.r)：除了基本的 R 支持，还提供了额外的工具和功能，如快捷的代码执行、R 包管理等。
- **R Debugger**：[安装链接](https://marketplace.visualstudio.com/items?itemName=RDebugger.r-debugger)：专门为 R 语言提供调试支持的插件，允许用户在 VScode 中设置断点、检查变量、逐行执行代码，极大提高了 R 语言开发中的调试效率，特别适合需要调试复杂脚本的用户。

### Stata 插件

以下 [Stata 插件]()特别适合需要跨平台工作和高效代码编辑的用户：

- **Stata Enhanced**：[安装链接](https://marketplace.visualstudio.com/items?itemName=kylebarron.stata-enhanced)：提供 Stata 代码的语法高亮、自动补全以及命令块执行功能，帮助用户直接在 VScode 中编写和运行 Stata 代码。
  
- **Stata Language**：[安装链接](https://marketplace.visualstudio.com/items?itemName=mdob2k.stata-language)：此插件为 Stata 提供了更丰富的语法高亮支持，能够识别特定的 Stata 语言结构，帮助用户更直观地编写和阅读 Stata 脚本，是日常脚本开发的实用工具。

- **stataRun**：[安装链接](https://marketplace.visualstudio.com/items?itemName=Yeaoh.stataRun)：通过此插件，用户可以直接在 VScode 中运行 Stata 代码，并将结果发送到 Stata 窗口。支持通过快捷键发送代码块，显著提升了跨编辑器与 Stata 的交互效率。

- **Code Runner**：[安装链接](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner)：虽然不是专为 Stata 开发，但支持在 VScode 中运行 Stata 代码，适合需要处理多种编程语言的开发者，可以简化多语言环境下的工作流管理。


### Python 插件

VScode 提供了多种 [Python 插件](https://marketplace.visualstudio.com/search?term=python&target=VSCode&category=All%20categories&sortBy=Relevance)，大大提升了 Python 得开发效率：

- **Python**：[安装链接](https://marketplace.visualstudio.com/items?itemName=ms-python.python)：微软官方提供的 Python 插件，支持自动补全、语法高亮、调试等功能，并集成了 Jupyter Notebook，适合 Python 开发者和数据科学家。
- **Pylance**：[安装链接](https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance)：这是 Python 插件的语言服务器扩展，提供更快速、更智能的代码分析、类型检查和导航功能，提升开发效率。
- **Jupyter**：[安装链接](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)：专为 Jupyter Notebook 提供支持，用户可以在 VScode 中创建、编辑和运行 Jupyter 笔记本，适合数据科学和机器学习工作。

### 思维导图插件

思维导图是帮助理清思路、组织信息的有力工具，以下是几款常用的 VScode 思维导图插件：

- **Markdown Preview Enhanced**：[安装链接](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced)：支持使用 `mermaid` 语法生成思维导图和流程图，适合文档编写和信息整理。
- **MindMap**：[安装链接](https://marketplace.visualstudio.com/items?itemName=hediet.vscode-drawio)：基于 `draw.io` 提供图形界面思维导图绘制工具，支持多种图表类型，方便可视化复杂的文档结构。
- **Mermaid Diagram**：[安装链接](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid)：支持基于 `mermaid` 语法的图表生成，能绘制思维导图、流程图等，

适合项目规划和结构展示。

### 幻灯片插件

VScode 支持 Markdown 格式的幻灯片制作，以下几款插件可以帮助你快速生成演示文稿：

- **Marp for VS Code**：[安装链接](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode)：通过 Markdown 语法快速生成演示文稿，支持导出 PDF、HTML 等格式。
- **Reveal.js**：[安装链接](https://marketplace.visualstudio.com/items?itemName=evilz.vscode-reveal)：基于 Reveal.js 的动态幻灯片生成插件，支持多种主题和动画效果，适合技术演讲和项目展示。
- **Slides**：[安装链接](https://marketplace.visualstudio.com/items?itemName=fcrespo82.markdown-slides)：支持多种幻灯片布局，适合技术分享和项目汇报，支持代码高亮和图表嵌入。



## 参考文献

1. Microsoft. Visual Studio Code Documentation. Available at: https://code.visualstudio.com/docs
2. Esben Petersen. Prettier - Code formatter. Available at: https://prettier.io/docs/en/index.html
3. GitLens Documentation. Available at: https://gitlens.amod.io
4. Marp Documentation. Available at: https://marp.app


&emsp;

## 相关推文

> Note：产生如下推文列表的 Stata 命令为：   
> &emsp; `lianxh 插件 VScode marp, md0 nocat`  
> 安装最新版 `lianxh` 命令：    
> &emsp; `ssc install lianxh, replace` 
  
  - [初虹](https://www.lianxh.cn/search.html?s=初虹), 2022, [Markdown-LaTeX：经管人的VSCode配置大全](https://www.lianxh.cn/details/1004.html), 连享会 No.1004.
  - [初虹](https://www.lianxh.cn/search.html?s=初虹), 2024, [让「记录」变得简单：Markdown使用详解](https://www.lianxh.cn/details/1456.html), 连享会 No.1456.
  - [宋森安](https://www.lianxh.cn/search.html?s=宋森安), 2021, [用Markdown制作幻灯片-五分钟学会Marp（上篇）](https://www.lianxh.cn/details/656.html), 连享会 No.656.
  - [宋森安](https://www.lianxh.cn/search.html?s=宋森安), 2021, [用Markdown制作幻灯片-五分钟学会Marp（下篇）](https://www.lianxh.cn/details/657.html), 连享会 No.657.
  - [王胜文](https://www.lianxh.cn/search.html?s=王胜文), 2023, [VScode编辑器：常用快捷键-Markdown专题](https://www.lianxh.cn/details/1174.html), 连享会 No.1174.
  - [连享会](https://www.lianxh.cn/search.html?s=连享会), 2020, [在 Visual Studio (vsCode) 中使用正则表达式](https://www.lianxh.cn/details/10.html), 连享会 No.10.
  - [连玉君](https://www.lianxh.cn/search.html?s=连玉君), 2022, [Marp幻灯片模板：用Markdown快速写幻灯片](https://www.lianxh.cn/details/1059.html), 连享会 No.1059.
  - [连玉君](https://www.lianxh.cn/search.html?s=连玉君), 2023, [Stata编程：快速查找Stata代码片段](https://www.lianxh.cn/details/1319.html), 连享会 No.1319.
  - [连玉君](https://www.lianxh.cn/search.html?s=连玉君), 2024, [VScode：实用 Markdown 插件推荐](https://www.lianxh.cn/details/1390.html), 连享会 No.1390.
  - [连玉君](https://www.lianxh.cn/search.html?s=连玉君), 2021, [用VScode正则表达式转换Markdown和LaTeX链接](https://www.lianxh.cn/details/839.html), 连享会 No.839.
  - [郭皑馨](https://www.lianxh.cn/search.html?s=郭皑馨), 2020, [vsCode+Stata：在 VScode 中编辑和运行Stata命令](https://www.lianxh.cn/details/151.html), 连享会 No.151.
