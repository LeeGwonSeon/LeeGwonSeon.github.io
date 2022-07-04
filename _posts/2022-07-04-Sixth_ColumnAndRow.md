---
layout: single
title:  "Column & Row"
categories: CSSLayout
tag: [CSS, CSSLayout, Flexbox, flex-diretion, Column, Row, blog]
toc: true
author_profile: false
sidebar:
    nav: "docs"
---

<div class="notice">
<h2>fourth study list.</h2>
<ul>
    <li>flex-direction의 Column과 Row</li>
    <p>전 시간은 Main axis(수평)와 Cross axis(수직)에 대한 개념에 대해서 공부하였습니다. 이번 시간은 Flex-direction의 Column(세로)과 Row(가로)에 대한 개념을 정리하였습니다.</p>
    <li>1. Flex-direction? </li>
    <li>2. Row </li>
    <li>3. Column</li>
</ul>
</div>

# 1. Flex-direction?

<h5>Flex-direction에 대해 간단히 정리 하자면 이번 시간의 핵심인 <span style="color:red">Column(세로)과 Row(가로)의 두 가지를 조작을 설정하는 곳</span>입니다.두 설정에 따라 <span style="color:red">Main Axis와 Cross Axis의 위치</span>가 바뀝니다.</h5>

# 2. Row

<h5>Row는 기본 설정으로 되어 있는 Main Axis와 같은 가로 방향의 설정입니다.</h5>

```python

flex-direction: row;

```

<h5>위와 같이 flex-direction: row로 설정을 하면 겉보기에는 차이가 없게 보이기도 합니다만 여기에서 중요한 것이 <span style="color:red">Main Axis와 Cross Axis의 방향</span>입니다.</h5>

![image-20220704193435097](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-04-Sixth_ColumnAndRow/image-20220704193435097.png?raw=true)

<h5>flex-direction: row 라고 설정을 하였을 시, <span style="color:red">Main Axis와 Cross Axis의 방향은 기본 설정과 같은 방향</span>으로 되어 있기 때문에 밑의 그림1 처럼 수평으로 보이게 됩니다.</h5>

![image-20220704193310218](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-04-Sixth_ColumnAndRow/image-20220704193310218.png?raw=true)

<h6>그림1</h6>

# 3. Column

<h5>flex=direction을 Column으로 설정할 경우, Row와 다른 점이 <span style="color:red">Main Axis와 Cross Axis의 위치가 바뀐다는 점</span>입니다. 이 부분에 있어서 이해하지 않은 상태에서 넘어가면 나중에 다시 이해하려고 할 때, 시간을 투자해야하니 확실하게 개념을 이해하고 넘어가는 걸 추천드립니다.</h5>

![image-20220704194410194](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-04-Sixth_ColumnAndRow/image-20220704194410194.png?raw=true)

<h5>위와 같이 <span style="color:red">Column은 Row의 가로축이 아닌 세로축으로 설정되어서 Main Axis와 Cross Axis의 방향 또한 가로축의 방향에 맞춰 위치가 바뀌기 때문에 디자인을 할 때 주의가 필요한 곳 중 하나</span>입니다. 가로 축의 설정에서는 밑의 그림2 의 방향으로 변경이 되니 참고하시기 바랍니다.</h5>

![image-20220704194909327](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-04-Sixth_ColumnAndRow/image-20220704194909327.png?raw=true)

<h5>그림2</h5>
