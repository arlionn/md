---
enableEmojiSyntax: true
print_background: true
puppeteer:
    author: 连玉君
    scale: 1.0           # 页面缩放    
 #   toc: true
 #   toc_depth: 2
    margin:
        top: 1.5cm
        bottom: 2cm
        right: 3.3cm
        left: 3.3cm
    timeout: 3000        # 延迟 3000 毫秒输出 HTML，进而转换为 PDF
    displayHeaderFooter: true
    headerTemplate:  '
        <div style="font-size: 10px; padding-top: 4px; text-align: center; width: 100%;">
            <span>连享会 · 文本分析专题</span>
          </div>'
    footerTemplate: '
        <div style="font-size: 10px; position: absolute; width: 100%; text-align: center; bottom: 0px;">
            <a href="https://www.lianxh.cn">www.lianxh.cn</a>
          <div style="font-size: 10px; position: absolute; width: 100%; text-align: right; bottom: 0px; right: 50px">
              <span class="pageNumber"></span>
          </div>
        </div>'
---  

# MPE 插件的使用

[toc]


<!-- @import "[TOC]" {cmd="toc" depthFrom=2 depthTo=3 orderedList=false} -->

<!-- code_chunk_output -->

- [MPE 插件简介](#mpe-插件简介)
  - [安装](#安装)
  - [主要功能](#主要功能)
- [设置](#设置)
- [更改主题](#更改主题)
- [TOC](#toc)
- [FDF 转换](#fdf-转换)
  - [方法 1：基于 Princexml](#方法-1基于-princexml)
  - [方法 2：chrome puppeteer (推荐)](#方法-2chrome-puppeteer-推荐)
- [代码块：添加行号和行高亮](#代码块添加行号和行高亮)

<!-- /code_chunk_output -->


## MPE 插件简介

**Markdown Preview Enhanced (MPE)** 是一款为 [**Visual Studio Code**](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced) 编辑器编写的**超级强大的** Markdown 插件。
这款插件意在让你拥有飘逸的 Markdown 写作体验。

在 [这里](https://github.com/shd101wyy/vscode-markdown-preview-enhanced/issues) 留言如果你发现了问题或者想要请求新的特性。[MPE 官方指南](https://github.com/shd101wyy/markdown-preview-enhanced/blob/master/docs/zh-cn/README.md)。

主要参考资料：

- [MPE 官网指南](https://shd101wyy.github.io/markdown-preview-enhanced/#/) &rarr; [中文](https://shd101wyy.github.io/markdown-preview-enhanced/#/zh-cn/)
  - Markdown 基本语法
  - MPE 插件的安装、导出 PDF和自定义 css
- [Markdown Preview Enhanced (MPE) 踩坑记录](https://blog.csdn.net/qq_43803536/article/details/124774578)




### 安装
- [用 Visual Studio Code 打造优雅的 Markdown 编辑环境](https://www.kindem.xyz/post/19/)
- [VS Code 版安装](zh-cn/vscode-installation.md)  
- [MPE 插件的安装]()

<!-- ![20231009125734](https://fig-lianxh.oss-cn-shenzhen.aliyuncs.com/20231009125734.png) -->

### 主要功能

*Note: 详情参见 [MPE 官方指南](https://github.com/shd101wyy/markdown-preview-enhanced/blob/master/docs/zh-cn/README.md)*

- 实时预览；支持 LaTeX 数学公式等
- 通过 Pandoc, Prince, Puppeteer 等将 .md 转换为 PDF, png 等。
- 制作和转换幻灯片
- TOC 生成和自定义
- 自定义预览 CSS
- 支持 mermaid 等流程图 / 时序图 以及各种其他种类的图形
- 嵌入 LaTeX, 渲染 TikZ, Chemfig 等图形

- 快捷键
  - 预览：`ctrl-shift-v`

## 设置

你可以在 VScode 编辑器中按 `Ctrl-shift-p` 键来打开 **Command Palette**。


## 更改主题

## TOC 

> 参见：[MPE 官网 - TOC 设置](https://github.com/shd101wyy/markdown-preview-enhanced/blob/master/docs/zh-cn/toc.md)

- `## 标题 4 {ignore=true}` 可以在目录中屏蔽 **标题 4**。

也可以在 .md 文件的题头部分通过编写 front-matter，进行更细致的设置：

~~~md
---
toc:
  depth_from: 1
  depth_to: 6
  ordered: false
---
~~~



## FDF 转换

> Note: 无论采用何种方式转换 PDF，都要预先关闭已经打开的同名 PDF 文件，否则会报错 (因为新转换的文件无法写入)。


### 方法 1：基于 Princexml 

目前测试结果来看，效果不如 Puppeteer 好。
- 缺点：
  - 字体不好看，需要修改
  - 首页右上角自动添加了 Prince 的 logo
  - 需要添加标记语句，以便显示页码和页脚等信息
  - 列表缩进有问题
  - 行间距太大
- 优点：
  - 可以直接显示被高亮的行

详情参见：[MPE 官网 - Prince 设置](https://github.com/shd101wyy/markdown-preview-enhanced/blob/master/docs/zh-cn/prince.md)

<https://www.princexml.com/doc/paged/#page-styles>

在使用VSCode插件“markdown-preview-enhanced”插件时，右击 Preview 页面，点击 **PDF (Prince)** 时，提示需要安装 `princexml`。安装方法如下：
- [VSCode问题："princexml" is required to be installed](https://juejin.cn/post/6844903748645421063)

### 方法 2：chrome puppeteer (推荐)

> 分页

在 markdown 文件中分页，用 html 代码解决。在需要分页的地方加入如下语句 (上下各空一行)   

`<div STYLE="page-break-after: always;"></div>`

不影响 html 显示，输出为 pdf 时候会分页。

- **markdown-preview-enhanced** (MPE) 插件 &rarr; Preview &rarr; 右击 &rarr; **Chrome (Puppeteer)** &rarr; **PDF**。
  - [官网介绍](https://github.com/shd101wyy/markdown-preview-enhanced/blob/master/docs/zh-cn/pdf.md)
- 调整 PDF 页面宽度，添加页码、页眉和页脚等信息等。 
  - 知乎：[Markdown Preview Enhanced (MPE) 输出PDF文档分页及页眉页脚](https://zhuanlan.zhihu.com/p/493494190)

> 为 PDF 添加页眉和页脚 

在 Markdown 文档头部添加如下信息，以调整 PDF 页面宽度，添加页码、页眉和页脚等信息等。

```html
---
enableEmojiSyntax: true
print_background: true
puppeteer:
    author: 连玉君
    scale: 1.0           # 页面缩放    
 #   toc: true
 #   toc_depth: 2
    margin:
        top: 1.5cm
        bottom: 2cm
        right: 3.3cm
        left: 3.3cm
    timeout: 3000        # 延迟 3000 毫秒输出 HTML，进而转换为 PDF
    displayHeaderFooter: true
    headerTemplate:  '
        <div style="font-size: 10px; padding-top: 4px; text-align: center; width: 100%;">
            <span>连享会 · 文本分析专题</span>
          </div>'
    footerTemplate: '
        <div style="font-size: 10px; position: absolute; width: 100%; text-align: center; bottom: 0px;">
            <a href="https://www.lianxh.cn">www.lianxh.cn</a>
          <div style="font-size: 10px; position: absolute; width: 100%; text-align: right; bottom: 0px; right: 50px">
              <span class="pageNumber"></span>
          </div>
        </div>'
---  
```

有关 puppeteer 转换 PDF 的其他设定，参见：
- [Puppeteer - PDFOptions interface](https://pptr.dev/api/puppeteer.pdfoptions)




## 代码块：添加行号和行高亮

~~~md
```stata {.line-numbers}
codes
```
~~~

例如：
```stata {.line-numbers}
sysuse "auto.dta", clear
sum price wei 
reg price wei mpg 
tw scatter mpg wei  ///
   title("Scatter graph")
```
#### 高亮指定行

*Note:* 这个仅在转换为网页 (.html) 时生效 (可以进一步通过 Google 浏览器转换为 PDF，`Ctrl+P`)。若直接转换为 PDF，则被高亮的行无法正常显示。 

~~~md
```stata {highlight=4-5}
…… codes ……
```
~~~

```stata {highlight=4-5}
sysuse "auto.dta", clear
sum price wei 
reg price wei mpg 
tw scatter mpg wei  ///
   title("Scatter graph")
```

```stata {highlight=3-5,.line-numbers}
sysuse "auto.dta", clear
*-----结果-------
  local s "using $Out\Table_xx.csv"  //执行时包括这一行会输出Excel表格
  local m "m1 m2 m3"
  esttab `m' `s', mtitle(`m') nogap compress replace   ///
         b(%6.3f) s(N r2_a) drop(`drop')   ///
         star(* 0.1 ** 0.05 *** 0.01)      ///
  		 addnotes("*** 1% ** 5% * 10%") 
```