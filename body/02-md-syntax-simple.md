# 简要 Markdown 语法

&emsp;

> Source: [markdownguide.org/cheat-sheet/](https://www.markdownguide.org/cheat-sheet/)

&emsp;

这份 Markdown 备忘单介绍了常用的 Markdown 语法。为了便于您快速了解基本的语法规则，这里略去了很多细节信息，详情参见 

- [基础语法](https://www.markdownguide.org/basic-syntax/) 
- [扩展语法](https://www.markdownguide.org/extended-syntax/) 
- [Markdown 语法 - Quarto](https://quarto.org/docs/authoring/markdown-basics.html)
- [Markdown 语法 - Github](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#using-emojis)

## 基础语法

以下是 [John Gruber](https://en.wikipedia.org/wiki/John_Gruber) 原始设计文档中列出的基本元素，所有 Markdown 应用程序都支持这些元素。

| 元素         | Markdown 语法                          |
| :------------ | :----------- |
| [标题](https://www.markdownguide.org/basic-syntax/#headings) | `# 一级标题`<br>`## 二级标题`<br>`### 三级标题`                        |
| [粗体](https://www.markdownguide.org/basic-syntax/#bold) | `**粗体文本**`                          |
| [斜体](https://www.markdownguide.org/basic-syntax/#italic) | `*斜体文本*`                      |
| [引用块](https://www.markdownguide.org/basic-syntax/#blockquotes-1) | `> 引用内容`                           |
| [有序列表](https://www.markdownguide.org/basic-syntax/#ordered-lists) | `1. 第一项`<br>`2. 第二项`<br>`3. 第三项` |
| [无序列表](https://www.markdownguide.org/basic-syntax/#unordered-lists) | `- 第一项`<br>&emsp; `  -  第一条`<br>`- 第二项`<br>`- 第三项`  |
| [代码](https://www.markdownguide.org/basic-syntax/#code) | \`代码`                                 |
| [水平线](https://www.markdownguide.org/basic-syntax/#horizontal-rules) | `---`                                    |
| [链接](https://www.markdownguide.org/basic-syntax/#links) | `[连享会主页](https://www.lianxh.cn)`       |
| [图片](https://www.markdownguide.org/basic-syntax/#images-1) | `![图片标题](/Fig/image.jpg)` |

## 扩展语法

这些元素扩展了基础语法，增加了更多功能，但并不是所有 Markdown 应用程序都支持这些元素。

| 元素      | Markdown 语法      |
| :-------- | :---------------- |
| [脚注](https://www.markdownguide.org/extended-syntax/#footnotes) | `这里有一句带脚注的句子。[^1]`<br>`[^1]: 这是脚注。` |
| [交叉引用](https://www.markdownguide.org/extended-syntax/#heading-ids) | `### 我的标题 {#sec-custom-id}`<br>参见 `@sec-custom-id`。      |
| [删除线](https://www.markdownguide.org/extended-syntax/#strikethrough) | `~~这句话被删除了。~~`                 |
| [任务列表](https://www.markdownguide.org/extended-syntax/#task-lists) | `- [x] 完成任务1`<br>`- [ ] 未完成任务2`<br>`- [ ] 未完成任务3` |
| [表情符号](https://www.markdownguide.org/extended-syntax/#emoji) [^1] | `这太有趣了！ :joy:`                |
| [高亮](https://www.markdownguide.org/extended-syntax/#highlight) | `请高亮显示==这些词==。` |
| [下标](https://www.markdownguide.org/extended-syntax/#subscript) | `H~2~O`                                  |
| [上标](https://www.markdownguide.org/extended-syntax/#superscript) | `X^2^`                                   |

[^1]: [可以复制粘贴的表情符号](https://www.markdownguide.org/extended-syntax/#copying-and-pasting-emoji)。

## 表格

```md
| 命令   | 范例                    |
|:------ |:-----------------------|
| xtreg  | `xtreg y x, fe`        |
| reghdfe| `reghdfe y x, a(id)`   |
```

| 命令   | 范例                    |
|:------ |:-----------------------|
| xtreg  | `xtreg y x, fe`        |
| reghdfe| `reghdfe y x, a(id)`   |


## 数学公式

```md
模型设定为：

$$y_{it} = \alpha_i + x_{it}\beta + u_{it}$$

其中，$y_{it}$ 为被解释变量，$\alpha_i$ 为个体效应。
```

模型设定为：

$$y_{it} = \alpha_i + x_{it}\beta + u_{it}$$

其中，$y_{it}$ 为被解释变量，$\alpha_i$ 为个体效应。
