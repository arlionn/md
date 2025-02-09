# Markdown 速览

> **作者**：连小白 (<lianxh@163.com>) 

[toc]

## 1. 何谓 Markdown ？
- 一种*标记语言*
  - 用 `# ` 标记 **标题**
  - 用 `- ` 标记 __列表__
- 用 \` 包围的代码会语法高亮
  - `regress` 命令很好用

```stata
sysuse "auto.dta"
regress mpg weight
```

## 2. 链接和图片

插入 [中山大学](http://www.sysu.edu.cn) 的 logo，可以用<br>`![图名(可省)](网址)`：

![](https://www.sysu.edu.cn/images/logo1.png){width=120pt fig-align="center"}

## 3. 数学公式

单行和行内公式分别用 `$$` 和 `$` 包围。

$$
y_i = x_i^2 \beta + u_i
$$

其中，$\beta$ 是待估参数。