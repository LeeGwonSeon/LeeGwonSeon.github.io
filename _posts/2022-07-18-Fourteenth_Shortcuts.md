---
layout: single
title:  "Shortcuts"
categories: CSSLayout
tag: [CSS, CSSLayout, Grid, column, row, header, content, nav, footer,Shortcuts, blog]
toc: true
author_profile: false
sidebar:
    nav: "docs"
---

<div class="notice">
<h2>Fourteenth_Shortcuts study list.</h2>
<ul>
    <li>Grid template Areas의 Shortcuts 개념 이해</li>
    <p>전 시간은 Grid의 Template Areas에 대한 개념에 대해서 공부하였습니다. 이번 시간은 Grid의 Template Areas의 Row and Column울 Shortcuts하는 방법을 정리하였습니다.</p>
    1. Grid의 Shortcuts
</ul>
</div>

# 1. Grid의 Shortcuts

<h5>전 시간에 Grid의 Template Areas을 사용하여 4가지 영역인 header, content, nav, footer의 설정의 Row와 Column에 대해서 공부하였습니다. 이번시간은 설정방법에 대하여 입력을 최소화하여 입력가능한 것에 대해 정리하였습니다.</h5>

```python

.grid{
    display: grid;
    grid-template-columns: repeat(4, 100px);
    grid-template-rows: repeat(4, 100px);
    gap: 10px;

  }

.header{
    background-color: chartreuse;
    grid-column: span 4;
}

.content{
    background-color: blue;
    grid-column: 1 / -2;
    grid-row: span 2;
}

.nav{
    background-color: blueviolet;
    grid-row: span 2;
}

.footer{
    background-color: coral;
    grid-column: span 4;
}

```

<h5>
위처럼 grid-column과 grid-row에서 시작점과 끝을 설정가능합니다. 여기에서 시작점인 1과 끝점의 -1에 대한 설명을 하면, <span style="color:red">-1은 1의 시작점과 마찬가지로 1의 반대편의 시작점 즉, 오른쪽 끝이 -1부터 설정이 가능</span>합니다. 또한, <span style="color:red">span을 입력하여 사용할 공간을 설정하게 되면 전 시간에 개념정리한 Row와 Column을 설정할 때 코드를 최소화</span>하여 끝낼 수 있습니다.</h5>

![image-20220718172416823](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-18-Thirteenth_Row%20and%20Column/image-20220718172416823.png?raw=true)

그림 1