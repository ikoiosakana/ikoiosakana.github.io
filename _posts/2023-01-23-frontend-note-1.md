---
title: "Front-end Note 1"
categories:
  - 前端
tags:
  - content
  - HTML
  - 前端
last_modified_at: 2023-01-23T13:25.000Z
---

前端介绍与 HTML 基础

## 前端介绍

### 前端技能构成

1. **HTML**: HyperText Markup Language, 网站的内容框架构建
2. **CSS**: Cascading Stylesheet, 美化外观
3. **JavaScript**: 实现功能
4. **Frameworks**: 如 React\Angular\Vue, 进行快速开发
5. **Version Control Systems**: Git, 管理版本, 共同开发

### 基础知识

1. URL: Uniform Resource Location
   - Resource: e.g. HTML 文件、图片、视频……
2. Client-Server model: Browser(client) —— Host(server)
   - 当 Browser 读到返回的 HTML 文件，会创建一个 DOM（Document Object Model)
   - 通过地址找到图片、字体等元素, 在这个过程中会再次进行 Request
   - 渲染（Render）

- HTML 对大小写不敏感
  - 惯例为除 DOCTYPE 外全部小写
- 【Ctrl+B】打开侧边栏
- 通过浏览器开发者工具中的样式测试网页布局

### Validation

- 检查 HTML 代码错误：validator.w3.org [https://validator.w3.org/]
- 检查 CSS 代码错误：jigsaw.w3.org/css-validator/ [https://jigsaw.w3.org/css-validator/]

## HTML 基础

- 【！+ Tab/Enter】可以生产基础 HTML 模板

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>

</body>
</html>
```

其中的 meta 元素

1. charset：字符集
2. viewport：网页提供的可视范围，包括初始宽度与放大系数
3. description：提供给搜索引擎的描述

### HTML 标签

- &lt;p> 段落
- &lt;em> 强调元素，帮助搜索引擎提取内容，default 为粗体
- &lt;strong>

- &lt;h1> ~ &lt;h6> 标题，每个网页都需要且只能有一个 h1 标题

#### 链接

- &lt;a> 锚点标签
  - href：超文本引用
  - download：点击下载，布尔
  - target：若值为`_blang`，则在新标签页打开网页

```
 <a href=""> text/<img src="" alt="">/…… </a>
```

- 【..】返回上一级

- 通过添加 id 来跳转至页面某处

```
<a href="#section-css">CSS</a>
<a href="#">Jump to Top</a>
```

#### 图片

- object-fit：若值为`cover`，则裁剪图片适应设置的图片大小

#### 视频

- control：显示控制按钮
- autoplay：自动播放
- loop：循环播放

```
<video src="">在此填入替换文本</video>
```

#### 列表

1. ul：无序列表
2. ol：有序列表

- liststyletype：样式
- li：list item

- 【control+enter】下方插入行

- 【ol>li\*3】快捷创建

3. dl：描述列表
   - dt：description term
   - dd：description detail

#### 表格

- &lt;tr> table row
- &lt;td> table dataceil 单元格
- &lt;th> table headerceil 表头

- &lt;thead>/&lt;tbody>/&lt;tfoot> 优化结构

- colspan：列扩展

##### CSS

- border：1px(边框宽度) solid（边框线类型） grey（颜色）
- 用`,`使 CSS 代码作用于多个对象

```
table, td {}
```

- 【按住 shift】选中多行，【按住 alt】上下移动

#### 容器

1. div：division
   - block-level：defalt 状态填充宽度为整行
2. span：
   - inline

- 【Ctrl+D】在选中一个词后可以多重编辑，按两次回车退出

##### semantic 容器

- &lt;article>
- &lt;figure>
- &lt;mark>
- &lt;time>

- &lt;figcaption>

- \<time datetime="2021-01-01 17:00">

###### 应用

```
<header>
    <nav>
        <ul>
            <li></li>
            <li></li>
            <li></li>
        </ul>
    </nav>
</header>
<main>
    <section>
        <h2></h2>
        <article></article>
    </section>
    <section>
        <h2></h2>
        <article></article>
    </section>
</main>
<aside></aside>
<footer></footer>
```

### HTML 转义字符

格式为：&相应字符；
e.g.
&copy;
&nbsp; 不换行字符

- 【lorem+词数】生成相应数量随机词
