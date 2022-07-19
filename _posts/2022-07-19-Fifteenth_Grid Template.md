---
layout: single
title:  "Grid Template"
categories: CSSLayout
tag: [CSS, CSSLayout, Grid, Template, header, content, nav, footer, fr, blog]
toc: true
author_profile: false
sidebar:
    nav: "docs"
---

<div class="notice">
<h2>Fifteenth-Grid Template study list.</h2>
<ul>
    <li>Grid template 개념 이해</li>
    <p>전 시간은 Grid의 Template Areas의 Row and Column울 Shortcuts하는 방법에 대한 개념에 대해서 공부하였습니다. 이번 시간은 Grid의 Template을 정리하였습니다.</p>
    1. Grid template
</ul>
</div>

# 1. Grid template

<h5>저번 시간에는 grid-template area 를 shortcuts로 최소화 하는 방법을 공부하였습니다. 이번 시간에는 더 간단하게 Grid를 설정 가능한 Grid template에 대해 정리하였습니다.</h5>

```python

HTML
<body>
    <div class="grid">
        <div class="header"></div>
        <div class="content"></div>
        <div class="nav"></div>
        <div class="footer"></div>
    </div>
</body>

CSS
.grid{
    display: grid;
    gap: 10px;
}
.header{
    background-color: chartreuse;
}

.content{
    background-color: blue;
}

.nav{
    background-color: blueviolet;
}

.footer{
    background-color: coral;
}

```

<h5>Grid Template에 대한 설명을 위해 4가지 영역인 header, content, nav, footer를 그림1 처럼 기본설정으로 하였습니다.</h5>

![image-20220719194059045](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-19-Fifteenth_Grid%20Template/image-20220719194059045.png?raw=true)

그림 1

<h5>Grid Template의 설명에 앞서 먼저, fr에 대한 개념을 정리하고 넘어가겠습니다. Flexbox에서는 px로 설정을 해도 바로 반응형으로 가능했습니다. 하지만 Grid에서 px로 설정을 할 경우 반응형이 아닌 px 크기 그대로 유지가 된 채로 화면을 줄여도 반응형이 되지 않았습니다. <span style="color:red">Grid에서 반응형으로 설정을 할 때는 px 대신 fr로 지정을 하게 되면 Flexbox처럼 반응형으로 설정이 가능</span>합니다.</h5>

```python

HTML
<body>
    <div class="grid">
        <div class="header"></div>
        <div class="content"></div>
        <div class="nav"></div>
        <div class="footer"></div>
    </div>
</body>

CSS
.grid{
    display: grid;
    gap: 5px;
    height: 50vh;
    grid-template: 
    "header header header header" 1fr
    "content content content nav" 2fr
    "footer footer footer footer" 1fr / 1fr 1fr 1fr 1fr;
    ;

  }

.header{
    background-color: chartreuse;
    grid-area: header;
}

.content{
    background-color: blue;
    grid-area: content;
}

.nav{
    background-color: blueviolet;
    grid-area: nav;
}

.footer{
    background-color: coral;
    grid-area: footer;
}

```

<h5>grid-template에서는 전전 시간에 배웠던 grid area와 사이즈를 설정을 할 수 있습니다. areas를 사용하는 방법은 동일하기 때문에 각 영역에 grid-area를 설정할 필요가 있습니다. <span style="color:red">grid-template에서 사용할 영역 설정과 사이즈를 설정하는데 fr을 사용하여, 각 영역에 grid-area를 설정</span>하게 되면 그림 2, 3 처럼 반응형으로 설정이 된 것을 확인하실 수 있습니다.</h5>

![image-20220719195834650](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-19-Fifteenth_Grid%20Template/image-20220719195834650.png?raw=true)

그림 2

![image-20220719195901462](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-19-Fifteenth_Grid%20Template/image-20220719195901462.png?raw=true)

그림 3