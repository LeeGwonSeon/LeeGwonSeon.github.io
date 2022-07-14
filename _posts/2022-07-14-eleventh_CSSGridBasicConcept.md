---
layout: single
title:  "CSS Grid Basic Concept"
categories: CSSLayout
tag: [CSS, CSSLayout, Flexbox, Grid, Basic Concept, blog]
toc: true
author_profile: false
sidebar:
    nav: "docs"
---

<div class="notice">
<h2>Eleventh study list.</h2>
<ul>
    <li>CSS Grid Basic Concept 개념 이해</li>
    <p>전 시간은 flex-basis에 대한 개념에 대해서 공부하였습니다. 이번 시간은 Grid의 기본 사용법을 정리하였습니다.</p>
    <li>1. Disadvantages of flexbox</li>
    <li>2. Grid 기본 사용법</li>
</ul>
</div>

# 1. Disadvantages of flexbox

<h5>flexbox는 1차원 레이아웃용으로 가능한 기능이기 때문에 flex-wrap의 설정을 wrap으로 설정을 하고, 웹화면을 축소하였을 경우 빈 공간이 생기게 되는 단점이 있습니다. 예를 들어</h5>


```python

.father {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
}

.child {
    flex-basis: 300px;
    background-color: blueviolet;
    color: white;
    font-size: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
}

```

<h5>위와 같이 father의 flex-wrap:wrap 으로 설정을 한 후, 웹화면을 축소하였을 시 밑의 그림1 처럼 두 번째 줄로 변경 되면서 빈 공간이 생기는 단점이 있습니다.</h5>

![image-20220714194944951](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-14-eleventh_CSSGridBasicConcept/image-20220714194944951.png?raw=true)

그림 1

<h5>위와 같은 단점을 보완가능 한 것이 Grid입니다.</h5>

# 2. Grid 기본 사용법

<h5>Grid는 2차원으로 레이아웃용의 기능을 가지고 있습니다. flexbox와는 다른점이 <span style="color:red">Column(세로)과 Row(가로)와 같은 섬세한 부분까지 설정 가능</span>합니다.</h5>

```python

.father {
    display: grid;
    grid-template-columns: 250px 250px 250px;
    grid-template-rows: 100px 50px 300px;
    gap: 10px;
}

.child {
    background-color: blueviolet;
    color: white;
    font-size: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
}

```

<h5>위와 같이display:grid로 설정이 되어 있는데, grid는 부모 역할을 하는 father에서 설정이 가능합니다.
    grid-template-column에서 1번째 부터 3번째 까지 250px로 설정을 하였습니다. 저 상태에서 <span style="color:red">child를 3개를 선언하게 되면 Column(세로)으로 설정이 가능</span>합니다. 또한, Column(세로)뿐만 아니라 Row(가로)로도 설정이 가능합니다. <span style="color:red">가로를 설정을 할 때는 grid-template-rows로 설정이 가능</span>한 데, grid-template-rows에서도 3개의 child의 크기를 설정한 것을 그림2 에서 확인 할 수 있습니다.
</h5>

![image-20220714200559066](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-14-eleventh_CSSGridBasicConcept/image-20220714200559066.png?raw=true)

그림 2

```python
<body>
    <div class="father">
        <div class="child">1</div>
        <div class="child">2</div>
        <div class="child">3</div>
        <div class="child">1</div>
        <div class="child">2</div>
        <div class="child">3</div>
        <div class="child">1</div>
        <div class="child">2</div>
        <div class="child">3</div>
    </div>
</body>
```

<h5>grid에서는 grid-template-column에서 설정한 child의 갯수 이상이 되었을 경우 그림2 처럼 줄바꿈이 자동으로 이루어지며, 줄바꿈과 동시에 grid-template-rows에서 설정한 child의 크기로 변환되는 섬세한 곳까지 설정이 가능한 2차원 레이아웃의 매력이 있습니다.</h5>
