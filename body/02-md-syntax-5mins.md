# Markdown 速览

> **作者**：连小白 (<lianxh@163.com>) 

---
[TOC]

## 何谓 Markdown ？

- 一种*标记语言*
  - 用 `# ` 标记 **标题**
  - 用 `- ` 标记 __列表__
- 可以添加代码块

```stata
sysuse "auto.dta", clear // 数据
```

## 链接和图片

[中山大学](http://www.sysu.edu.cn) logo，可以用  
`![图名](网址或路径)`：

![](https://www.sysu.edu.cn/images/logo1.png){width=150pt}

## 数学公式

单行和行内公式分别用 `$$` 和 `$` 包围。

$$
y_i = x_i^2 \beta + u_i
$$

其中，$\beta$ 是待估参数。