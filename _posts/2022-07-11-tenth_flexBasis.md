---
layout: single
title:  "flex-basis"
categories: CSSLayout
tag: [CSS, CSSLayout, Flexbox, flexbasis,  blog]
toc: true
author_profile: false
sidebar:
    nav: "docs"
---

<div class="notice">
<h2>tenth study list.</h2>
<ul>
    <li>flex-basis 개념 이해</li>
    <p>전 시간은 flex-grow와 flex-shrink에 대한 개념에 대해서 공부하였습니다. 이번 시간은 flex-basis에 대한 개념을 정리하였습니다.</p>
    <li>1. flex-basis</li>
</ul>
</div>

# 1. flex-basis
<h5>flex-basis는 겉보기에는 width가 같은 기능으로 보이겠지만 전시간에 배웠던 flex-grow로 child의 크기가 커지는 것과 flex-shrink로 child의 크기가 작아지는 것 또는 화면이 작아졌을 때 child가 구겨지는 현상, 그 전 단계의 child의 초기 크기를 설정하는 기능입니다.</h5>

```python
.child {
    flex-basis: 300px;
    display: flex;
    justify-content: center;
    align-items: center;
}


.child:nth-child(2) {
    background-color: black;
    flex-grow: 1;
}
```

<h5>위와 같이 child 전체를 flex-basis: 300px 로 지정을 해주고, 두 번째 child에게 flex grow를 설정해 줄 경우 밑의 그림1 과 같은 결과가 나타납니다.</h5>

![image-20220711185644876](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-11-tenth_flexBasis/image-20220711185644876.png?raw=true)

그림1

<h5>flex-basis는 오직 main axis에서만 사용이 가능합니다.
지금의 그림1 의 경우는 row에서의 설정이지만 column을 사용해 main axis의 위치를 변경하는 것도 가능합니다.</h5>

```python
.child {
    flex-basis: 300px;
    flex-direction: column;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 50vh;
    height: 50vh;
}


.child:nth-child(2) {
    background-color: black;
    flex-grow: 1;
}
```
<h5>위와 같이 flex-direction을 column으로 설정을 하여 width과 height의 크기를 지정하게 되면 그림2 와 같이 main axis의 방향을 cross axis으로 전환하는 것도 가능합니다.</h5>

![image-20220711190918597](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-11-tenth_flexBasis/image-20220711190918597.png?raw=true)

그림2