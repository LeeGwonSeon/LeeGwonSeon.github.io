---
layout: single
title:  "Row and Column"
categories: CSSLayout
tag: [CSS, CSSLayout, Grid, column, row, header, content, nav, footer, blog]
toc: true
author_profile: false
sidebar:
    nav: "docs"
---

<div class="notice">
<h2>Thirteenth_Row and Column study list.</h2>
<ul>
    <li>Grid template Areas의 Row and Column의 개념 이해</li>
    <p>전 시간은 Grid의 Template Areas에 대한 개념에 대해서 공부하였습니다. 이번 시간은 Grid의 Template Areas의 Row and Column울 정리하였습니다.</p>
    1. Grid의 Row and Column
</ul>
</div>

# 1. Grid의 Row and Column

<h5>전 시간에 Grid의 Template Areas을 사용하여 4가지 영역인 header, content, nav, footer의 설정하는 방법에 대해서 공부하였습니다. 그 개념을 이해하기 위해 이번에는 areas를 사용하지 않고, Row와 Column 만을 사용하여 개념을 이해하고 넘어가도록 하겠습니다.</h5>

```python

HTML
<div class="grid">
        <div class="header"></div>
        <div class="content"></div>
        <div class="nav"></div>
        <div class="footer"></div>
    </div>

CSS
.grid{
    display: grid;
    grid-template-columns: repeat(4, 100px);
    grid-template-rows: repeat(4, 100px);
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

<h5>기본적인 header, content, nav, footer를 설정하여 areas 영역인 Row와 Column의 개념을 이해하고 넘어가겠습니다. area영역을 사용한 것에 대해 기본 지식으로 어떤 작용을 하는지 알기 위해서 입니다.</h5>

![image-20220718171143866](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-18-Thirteenth_Row%20and%20Column/image-20220718171143866.png?raw=true)

그림1

<h5>그림 1에 대한 설명을 하자면 column과 row가 1부터 5까지의 영역이 있습니다. 그림 2을 참고하시면 아시겠지만, 이처럼 설정한 1부터 5의 영역을 <span style="color:red">grid-column-start와 grid-column-end 그리고 grid-row-start와 grid-row-end로 설정이 가능</span>합니다.</h5>

![image-20220718171750390](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-18-Thirteenth_Row%20and%20Column/image-20220718171750390.png?raw=true)

그림 2


```python

.grid{
    display: grid;
    grid-template-columns: repeat(4, 100px);
    grid-template-rows: repeat(4, 100px);
    gap: 10px;

  }

.header{
    background-color: chartreuse;
    grid-column-start: 1;
    grid-column-end: 5;
}

.content{
    background-color: blue;
    grid-column-start: 1;
    grid-column-end: 4;
    grid-row-start: 2;
    grid-row-end: 4;
}

.nav{
    background-color: blueviolet;
    grid-row-start: 2;
    grid-row-end: 4;
}

.footer{
    background-color: coral;
    grid-column-start: 1;
    grid-column-end: 5;
}

```

<h5>위처럼 grid-column-start와 grid-column-end 그리고 grid-row-start와 grid-row-end에서 시작 영영과 끝 영역의 범위를 설정을 해주게 되면 <span style="color:red">areas에서의 header, content, nav, footer 처럼 설정이 가능하게 되는데, 이것이 areas에서 설정 되고 있는 column과 row의 개념</span>입니다.</h5>

![image-20220718172416823](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-18-Thirteenth_Row%20and%20Column/image-20220718172416823.png?raw=true)

그림 3