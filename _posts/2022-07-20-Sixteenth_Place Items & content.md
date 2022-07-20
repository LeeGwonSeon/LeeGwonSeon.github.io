---
layout: single
title:  "Place Items & content"
categories: CSSLayout
tag: [CSS, CSSLayout, Grid, Template, header, content, nav, footer, fr, blog]
toc: true
author_profile: false
sidebar:
    nav: "docs"
---

<div class="notice">
<h2>Sixteenth_Place Items & content study list.</h2>
<ul>
    <li>Grid template 개념 이해</li>
    <p>전 시간은 Grid의 Template에 대한 개념에 대해서 공부하였습니다. 이번 시간은 Grid의 Place Items와  Place content 정리하였습니다.</p>
    1. Place Items
    2. Place content
</ul>
</div>

# 1. Place Items

<h5>이번 시간은 Place Items 에 대해 개념을 정리하였습니다.
place Items는 justify-Items와 align-items를 동시에 설정이 가능한 기능을 가지고 있습니다. 그것에 대한 설명을 위해 기본 설정을 하였습니다.</h5>

```python
HTML
<body>
    <div class="grid">
        <div class="header">header</div>
        <div class="content">content</div>
        <div class="nav">nav</div>
        <div class="footer">footer</div>
    </div>
</body>

CSS
 .grid{
    display: grid;
    gap: 5px;
    height: 50vh;
    ;

    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: repeat(4, 1fr);
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

![image-20220720195113770](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-20-Sixteenth_Place%20Items%20%26%20content/image-20220720195113770.png?raw=true)

그림 1

<h5>위의 그림 1 처럼 설정을 한 상태에서 Place Items을 사용하여 이벤트 기능을 추가해보겠습니다.</h5>

```python
HTML
<body>
    <div class="grid">
        <div class="header">header</div>
        <div class="content">content</div>
        <div class="nav">nav</div>
        <div class="footer">footer</div>
    </div>
</body>

CSS
 .grid{
    display: grid;
    gap: 5px;
    height: 50vh;
    ;

    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: repeat(4, 1fr);
    place-items: stretch center;
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
<h5>grid의 안에 place-items를 설정하고 첫번째 칸에 stretch을 입력하고 두번째 칸에 center를 입력하여서 그림 2와 같은 설정을 하였습니다.</h5>

![image-20220720195908089](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-20-Sixteenth_Place%20Items%20%26%20content/image-20220720195908089.png?raw=true)

그림 2

<h5>그림 2를 보시면 아시겠지만, <span style="color:red">첫번 째 칸에서는 align-items와 같은 수직에 설정이 가능하며, 두번 째 칸에서는 justify-items와 같은 수평의 설정이 가능</span>합니다. 단, 위와 같은 설정을 주기 위해서는 width과 height을 설정을 하지 않은 상태에서는 설정을 해도 화면에 나타나지 않으니 주의가 필요합니다.</h5>

# 2. Place content
<h5>Place content에서는 개념을 이해하기 위해 fr을 사용하지 않고 일반 px로 설정을 하여 개념을 정리하겠습니다. 정리에 앞서 <span style="color:red">content는 100% width으로 설정</span>이 되니 참고하시기 바랍니다.</h5>

```python

HTML
<body>
    <div class="grid">
        <div class="header">header</div>
        <div class="content">content</div>
        <div class="nav">nav</div>
        <div class="footer">footer</div>
    </div>
</body>

CSS
 .grid{
    display: grid;
    gap: 5px;
    height: 50vh;
    height: 100vh;
    grid-template-columns: repeat(4, 100px);
    grid-template-rows: repeat(4, 100px);
  }

```

<h5>repeat의 설정을 fr이 아닌 100px로 설정하여 그림 3과 같은 정사각형의 4가지 영역들을 준비하였습니다.</h5>

![image-20220720201918751](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-20-Sixteenth_Place%20Items%20%26%20content/image-20220720201918751.png?raw=true)

그림 3

<h5><span style="color:red">place-content에서도 place-items와 같은 순서로 첫 번째 칸에서는 align-content와 같은 수직을 설정하며, 두 번째 칸에서는 justify-content의 수평을 설정이 가능</span>합니다.</h5>

```python

HTML
<body>
    <div class="grid">
        <div class="header">header</div>
        <div class="content">content</div>
        <div class="nav">nav</div>
        <div class="footer">footer</div>
        <div class="header">header</div>
        <div class="content">content</div>
        <div class="nav">nav</div>
        <div class="footer">footer</div>
        <div class="header">header</div>
        <div class="content">content</div>
        <div class="nav">nav</div>
        <div class="footer">footer</div>
        <div class="header">header</div>
        <div class="content">content</div>
        <div class="nav">nav</div>
        <div class="footer">footer</div>
    </div>
</body>

CSS
.grid{

    background: darkgray;
    color: white;
    display: grid;
    gap: 5px;
    height: 100vh;
    grid-template-columns: repeat(4, 100px);
    grid-template-rows: repeat(4, 100px);
    place-content: end center;
  }

```
<h5>place-content의 개념이해를 돕기위해 각 4가지 영역을 4개씩 추가와 height를 100vh로 설정하여 background color 안에서의 위치를 그림 4에서 확인을 쉽게 하였습니다.</h5>

![image-20220720202701456](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-20-Sixteenth_Place%20Items%20%26%20content/image-20220720202701456.png?raw=true)

그림 4

<h5>place-content에서 첫 번째 칸에 end로 설정한 대로 child가 수직의 끝으로 이동한 것과 두 번째 칸에 center로 설정한 대로 수평의 중간에 이동한 것을 확인하실 수 있습니다.</h5>
