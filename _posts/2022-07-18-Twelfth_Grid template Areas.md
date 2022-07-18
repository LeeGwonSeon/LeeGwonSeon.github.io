---
layout: single
title:  "Grid Template Areas"
categories: CSSLayout
tag: [CSS, CSSLayout, Grid, Area, column, row, header, content, nav, footer, blog]
toc: true
author_profile: false
sidebar:
    nav: "docs"
---

<div class="notice">
<h2>Twelfth_Grid template Areas study list.</h2>
<ul>
    <li>Grid template Areas 개념 이해</li>
    <p>전 시간은 Grid의 기본 사용법에 대한 개념에 대해서 공부하였습니다. 이번 시간은 Grid의 Template Areas를 정리하였습니다.</p>
    1. 4area(header, content, nav, footer)<br>
    2. Grid Template Areas 사용법
</ul>
</div>

# 1. 4area(header, content, nav, footer)

<h5>웹 화면의 기본적인 영역으로는 header, content, nav, footer로 되어 있습니다. 보통 웹화면을 개발하는데 있어서 기본적인 영역을 기준으로 프론트엔드의 개발을 하게 됩니다.</h5>

```python

HTTML
<div class="grid">
        <div class="header"></div>
        <div class="content"></div>
        <div class="nav"></div>
        <div class="footer"></div>
    </div>

CSS
.grid{
    display: grid;
    grid-template-columns: repeat(4, 200px);
    grid-template-rows: repeat(4, 200px);
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

<h5>4가지 영역을 이해하기 위해 위와 같이 기본적인 header, content, nav, footer를 설정하였습니다. 화면에서 설정한 4가지 영역을 표시하기 위해서는 <span style="color:red">grid-template-columns과 grid-template-row 에서 4번의 200px 를 입력하는 방법</span>도 있지만 그것을 간단하게 하기 위한 방법으로 <span style="color:red">repeat(4, 200px)으로 설정하는 방법</span>이 있습니다.</h5>

![image-20220718154625443](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-18-Twelfth_Grid%20template%20Areas/image-20220718154625443.png?raw=true)

그림 1

<h5>그림 1 과 같이 column과 row에서 repeat(4, 200px)으로 설정한 결과가 나타납니다. <span style="color:red">repeat의 첫 칸에서는 몇 번이나 지정을 할 건지 입력하는 란과 2번째 칸에서는 사이즈를 얼마나 할 것인지 지정</span>을 할 수 있습니다.</h5>

# 2. Grid Template Areas 사용법
<h5>위에서 기본적으로 설정한 header, content, nav, footer를 Grid에서 어떻게 설정이 가능한 지 알아보겠습니다.</h5>

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
    grid-template-columns: repeat(4, 200px);
    grid-template-rows: 100px repeat(2, 200px) 100px;
    grid-template-areas: 
    "header header header header"
    "content content content nav"
    "content content content nav"
    "footer footer footer footer";
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

<h5>위의 CSS 영역에서 <span style="color:red">grid-template-areas을 보시면 아시겠지만 area에서 무엇을 사용할 것인지 지정가능</span>합니다. 예를 들어 첫 줄은 어떤것을 사용할 것인가 두 번째 줄은 어떤것을 사용할 것인가 3번째는? 4번째는? 이렇게 4번째 줄까지 어떤 것을 사용할 것인지 지정을 해줍니다. 하지만 grid-template-areas에서 지정을 하였다고 바로 적용되는 것은 아닙니다. <span style="color:red">grid 부모 영역에서 grid-template-areas의 설정을 header, content, nav, footer에 연결</span>을 시켜줘야 가능하게 됩니다. 그 방법으로 <span style="color:red">각 4가지 영역에 grid-area로 grid에서 설정한 4가지 영역 중 어떤 영역을 사용할 것인지 지정</span>을 해야지 사용이 가능합니다.</h5>

![image-20220718160333963](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-18-Twelfth_Grid%20template%20Areas/image-20220718160333963.png?raw=true)

그림 2