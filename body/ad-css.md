# 自定义 CSS

CSS（层叠样式表）是一个强大的工具，可以控制网页的布局和外观。在使用 Markdown 时，初看起来你可能不需要 CSS，但随着文档内容的复杂性增加，添加自定义样式能够极大地提升文档的展示效果。

本章介绍何时使用 CSS、如何自定义 CSS，以及如何在常用的 Markdown 工具（如 VScode、Typora、Quarto 和 Marp）中使用 CSS。

## 1. 何谓 CSS？

Markdown 是一种**文本标记语言**，它的主要作用在于「标记」，例如：

- 用 `## Why?` 将文本 `Why?` 标记为二级标题；
- 用 `**粗人**` 将 `粗人` 二字标记为粗体字。

因此，使用 Markdown 写作时，你只需专注于「内容创作」，而无需关注排版问题。

那么，文档的排版和美化效果是如何实现的呢？这主要借助 **CSS (层叠样式表)** 来控制，包括字体、字号、颜色、段落行距、页面布局等。

简言之，Markdown 负责**内容**的表达，而 CSS 则负责内容的**排版**和**美化**

多数 Markdown 编辑器都会提供一组默认的 .css 文件，这些文件定义了文档在编辑器中的显示样式。你可以新增或修改系统默认的 .css 文件，以实现个性化需求。

@fig-md-css-vue-lian 是我定义的 **vue-lian.css** 模板 ([下载](https://www.lianxh.cn/details/1426.html)) 的渲染效果：

![](https://fig-lianxh.oss-cn-shenzhen.aliyuncs.com/20220501155804.png){#fig-md-css-vue-lian}

## 2. 如何自定义 CSS？

自定义 CSS 通常涉及创建一个样式表（`.css` 文件），并在其中定义各类元素的样式。详情参见：
- [菜鸟教程 CSS](https://www.runoob.com/css/css-tutorial.html) 或 [W3School 教程 CSS](https://www.w3school.com.cn/css/index.asp)

### 2.1 编写 CSS

CSS 的基本语法非常简单。你通过选择器来制定某类 HTML 元素，然后定义它们的样式。例如：

```css
/* 二级标题 */
h2 {
  font-family: 'Arial', sans-serif;
  color: #2c3e50;   /* 标题颜色 */
  font-size: 1.3em; /* 字体大小：默认值的 1.3 倍 */
}

/* 段落元素 */
p {
  font-family: 'Georgia', serif;
  line-height: 1.6; /* 行间距 */
  color: #34495e;   /* 文本颜色 */
}
```

上述代码选择了 `h2` 和 `p` 元素，并为它们定义了字体、颜色和字体大小等样式。

### 2.2 深入了解 CSS 样式

除了基础的文本和颜色设置，CSS 还能做到更复杂的布局控制，例如：

- **盒模型**：CSS 中的盒模型决定了页面元素的尺寸和布局。它包括边距（margin）、边框（border）、内边距（padding）和内容（content）。
  
  示例：
  ```css
  div {
    margin: 20px;
    padding: 10px;
    border: 1px solid #ccc;
  }
  ```

<!-- ### 2.3 扩展阅读

要深入了解 CSS 的更多属性和技巧，可以参考如下资料：

- [MDN CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)：CSS 入门和全面文档，适合初学者和进阶用户 
- [CSS-Tricks](https://css-tricks.com/)：提供丰富的教程和 CSS 技巧  -->



## 3. 如何使用 CSS？

### 3.1 在 VScode 中使用 CSS

在 VScode 中，Markdown 渲染可以通过扩展和一些设置进行自定义。

1. **安装 Markdown Preview Enhanced 扩展**：在 VScode 中，打开侧边栏的扩展面板（快捷键：`Ctrl+Shift+X`），搜索 `Markdown Preview Enhanced`，然后点击安装。
2. **链接 CSS 文件**：安装完成后，打开你的 Markdown 文件，点击右上角的设置按钮，在下拉菜单中选择“Settings”。
   
   在设置窗口中，找到 `markdown.preview.styles` 选项，点击“Edit in settings.json”。
   
   在 `settings.json` 文件中，添加以下内容：
   
   ```json
   "markdown.preview.styles": [
     "path/to/your/custom.css"
   ]
   ```
   
   这样就能将你的自定义 CSS 文件应用到 VScode 中的 Markdown 预览中。

3. **预览 Markdown**：完成 CSS 设置后，可以通过 `Ctrl + Shift + V` 来预览带有自定义样式的 Markdown 文件。

### 3.2 在 Typora 中使用 CSS

Typora 是一个支持 Markdown 的桌面应用，内置了对自定义 CSS 的支持。

1. **打开 Typora 设置**：点击 Typora 界面左上角的 `偏好设置`（Preferences），然后点击 `外观`（Appearance）。
2. **找到并编辑主题文件**：在 `高级`（Advanced）选项中，点击“打开主题文件夹”。
3. **修改 CSS**：在主题文件夹中，你可以编辑现有的 CSS 文件，或创建一个新的 CSS 文件。
4. **应用 CSS**：修改或添加 CSS 后，保存文件并返回 Typora，你会看到效果立即生效。

如果你不想修改 CSS 文件，也可以直接下载现成的 CSS 样式文件。

### 3.3 在 Quarto 中使用 CSS

Quarto 允许用户通过在 YAML 头部配置文件中直接引用 CSS 文件来自定义样式。

1. **创建或编辑 CSS 文件**：编写一个 `.css` 文件，定义你需要的样式规则。
2. **引用 CSS 文件**：在 Quarto 文件的 YAML 头部，添加如下内容来引用 CSS 文件：

   ```yaml
   format: html
   css: path/to/your/custom.css
   ```

3. **渲染文档**：引用 CSS 后，当你渲染 Quarto 文件时，CSS 样式将会应用到生成的 HTML 页面上。

### 3.4 在 Marp 中使用 CSS

Marp 是一个将 Markdown 转换为 PPT 的工具，它也支持自定义 CSS。你可以在 Marp 的头部 YAML 中直接写入 CSS 格式设定，以方便分享文档。

1. **编辑 YAML 头部**：在 Marp 的 Markdown 文件中，打开头部 YAML 配置块，添加 CSS 相关设置：

   ```yaml
   ---
   marp: true
   theme: custom
   css: path/to/your/custom.css
   ---
   ```

2. **定义样式**：你可以在 `path/to/your/custom.css` 中定义你希望应用的样式。例如，你可以控制 PPT 的背景颜色、文字大小等。

3. **生成 PPT**：设置完成后，使用 Marp 命令生成 PPT 文件。所有的 CSS 样式将在生成的幻灯片中自动生效。

如果你不想自己写 CSS 样式，可以从以下网站下载一些现成的样式：

- [CSS Frameworks](https://www.w3schools.com/css/css_frameworks.asp)（提供多种 CSS 框架）
- [Free CSS](https://www.free-css.com/)（提供免费的 CSS 模板和样式）

## 4. 总结

CSS 是美化 Markdown 文档的重要工具。通过编写和应用 CSS，你可以实现更丰富的视觉效果、排版和响应式设计。在 VScode、Typora、Quarto 和 Marp 等工具中，你都可以方便地使用和自定义 CSS 样式。掌握 CSS 后，你的 Markdown 文档不仅在内容上专业，外观上也将更加精致。

此外，使用 CSS 可以帮助你控制 Markdown 转换为 PDF 时的页面边距、行距等输出效果，让你的文档更加精美和符合出版标准。

了解何时需要自定义样式，并根据需求灵活运用 CSS，能让你的 Markdown 文档更具吸引力和可读性。