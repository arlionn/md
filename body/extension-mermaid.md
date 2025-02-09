# mermaid: 思维导图插件

## 简单示例

<img style="width: 400px" src="https://fig-lianxh.oss-cn-shenzhen.aliyuncs.com/20230930095645.png">

![20230930103526](https://fig-lianxh.oss-cn-shenzhen.aliyuncs.com/20230930103526.png)



## 安装和应用环境

### 在线编写并输出为图片

- <https://mermaid.live/>

### Typora 
- 无需安装任何插件，因为 Typora 自带 mermaid 功能。 
- 语法结构与在 VScode 中完全一致，因此，可以将 VScode 中写好的 Markdown 文档，用 Typora 转换为 PDF 或 Word 文档。 

### VScode 
- 安装插件：按快捷键 **Ctrl+Shift+X**，搜索 `mermaid`，根据需要安装相关插件。推荐如下两个基本插件
  - `Markdown Preview Mermaid Support`，用于转换 Mermaid 对象
  - `vscode-mermaid-syntax-highlight`，语法高亮
- 制作 Mermaid 图形：将 mermaid 代码用代码块包围，即头部为 **```mermaid**，尾部为 **\`\`\`**
  ````md
  ```mermaid
     codes
  ```
  ````

### Quarto
- [Quarto - Mermaid and Graphviz diagrams](https://quarto.org/docs/authoring/diagrams.html)

### Marp 
使用 [Marp](https://www.lianxh.cn/news/148555c4f20ce.html) 插件制作幻灯片时，需要用 `<div class="mermaid">` 和 `</div>` 包围 mermaid 代码。


> 参考资料：

- [Integrating Mermaid diagrams into Markdown slides](https://github.com/hakimel/reveal.js/issues/1082)

````md
```html
<div class="mermaid">
graph LR 
    Start(想读博士) --> IsFile{能吃苦不?}
    IsFile -->| No | A[go away]
    IsFile -->| Yes| B[come on]
</div>
```
````

输出效果：

```mermaid
graph LR 
    Start(想读博士) --> IsFile{能吃苦不?}
    IsFile -->| No | A[go away]
    IsFile -->| Yes| B[come on]
```






## 参考资料
- Mermaid 官网：[Diagramming and charting tool](http://mermaid.js.org/intro/)
  - 提供了语法基础，常用图形的绘制案例
  - 在线绘制 Mermaid：<https://mermaid.live/>
  - [github](https://github.com/mermaid-js/mermaid)
- 知乎，[Markdown 进阶技能：用代码画流程图](https://zhuanlan.zhihu.com/p/69495726)
- [Mermaid 语法大全](https://blog.csdn.net/weixin_45017098/article/details/131189766)，这个非常全面



## 形状和模板

> Source: [Mermaid 官网 - Flowchart](https://mermaid.js.org/syntax/flowchart.html)
```mermaid
flowchart LR
    id1[(Database)] --> id2[( Model)] --> id3[(Results)]
```

````md
```mermaid
graph LR 
    Start(想读博士) --> IsHard{能吃苦不?}
    IsHard -->| No | A[go away]
    IsHard -->| Yes| B[come on]
```
````


```mermaid
graph LR 
    Start(想读博士) --> IsHard{能吃苦?}
    IsHard -->| No | A[go away]
    IsHard -->| Yes| B[come on]
```


## 简单示例

```mermaid
graph TB
    Start(开始) --> Open[打开冰箱门]
    Open --> Put[把大象放进去]
    Put[把大象放进去] --> IsFit{"冰箱小不小？"}
    
    IsFit -->|不小| Close[把冰箱门关上]
    Close --> End(结束)
        
    IsFit -->|小| Change[换个大冰箱]
    Change --> Open
```

## 进化图
> Source: [Mermaid语法大全](https://blog.csdn.net/weixin_45017098/article/details/131189766)
```mermaid
gantt
  title Git 进化史
  dateFormat YYYY-MM-DD
  section 远古时代
  创建 Git :a1, 2005-04-12, 15d
  section 现代化时代
  GitHub 购买 Git :a2, 2018-06-04, 1d
  section 近期时 
  Microsoft 收购 GitHub :a3, 2018-06-04, 1d
```

1. `title`：定义 Git 图的标题。
2. `dateFormat`：定义日期格式。
3. `section`：定义不同时间段。
4. 使用 `:` 分隔任务名称和 ID。
5. 使用 `,` 分隔任务 ID、开始日期和持续天数。

## Flow Chart

```mermaid
%%{init: {"flowchart": {"htmlLabels": false}} }%%
flowchart LR
    markdown["`This **is** _Markdown_`"]
    newLines["`Line1
    Line 2
    Line 3`"]
    markdown --> newLines
```

## Gantt diagram
> Source: [Mermaid: Diagramming and charting tool](http://mermaid.js.org/intro/)
Code:
```mermaid
gantt
dateFormat  YYYY-MM-DD
title Adding GANTT diagram to mermaid
excludes weekdays 2014-01-10

section A section
Completed task            :done,    des1, 2014-01-06,2014-01-08
Active task               :active,  des2, 2014-01-09, 3d
Future task               :         des3, after des2, 5d
Future task2               :         des4, after des3, 5d
```
## 
```mermaid
mindmap
  root((mindmap))
    Origins
      Long history
      ::icon(fa fa-book)
      Popularisation
        British popular psychology author Tony Buzan
    Research
      On effectivness<br/>and features
      On Automatic creation
        Uses
            Creative techniques
            Strategic planning
            Argument mapping
    Tools
      Pen and paper
      Mermaid
```


```mermaid
mindmap
  root((研究设计))
    ::icon(fa fa-rocket)  
    提出问题
    ::icon(fa fa-question-circle)
      现实观察
      ::icon(fa fa-eye)
      文献争议
      ::icon(fa fa-arrows-alt)
    研究方法
    ::icon(fa fa-wrench)
    研究假设
    ::icon(fa fa-blind) 
```