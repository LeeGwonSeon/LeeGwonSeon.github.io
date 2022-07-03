---
layout: single
title:  "Main axis & Cross axis"
categories: CSSLayout
tag: [CSS, CSSLayout, Flexbox, Mainaxis, Crossaxis, blog]
toc: true
author_profile: false
sidebar:
    nav: "docs"
---

<div class="notice">
<h2>third study list.</h2>
<ul>
    <li>flexbox의 Main axis & Cross axis</li>
    <p>전 시간에서는 flexbox의 선언 방법과 개념에 대해서 공부하였습니다. 이번 시간은 Main axis(수평)와 Cross axis(수직)에 대한 개념을 이해하면서 정리하였습니다.</p>
    <li>1. Main axis(Horizontal axis) </li>
    <li>2. Cross axis(Vertical) </li>
</ul>
</div>

# 1. Main axis(Horizontal axis)

<h5><span style="color:red">Main axis(Horizontal axis)는 justify-content로 설정 가능</span>하며, 수평(가로)축의 위치 설정의 기능이 있습니다. 과거에는 Margin으로 조작을 하는데 복잡하고 시간이 걸렸지만, <span style= "color:red">Main axis에서는 수평의 위치의 설정이 되어있는 상태라서 작성을 하는데 시간을 단축</span>할 수 있습니다.</h5>

```python

justify-content: space-around;

```
<h5>간단한 예로 justify-content의 설정을 space-around로 설정을 하였을 시, <span style="color:red">수평축의 일정 간격을 벌리는 것이 가능</span>합니다.<br>
(그림1 참조)</h5>

![image-20220703224010695](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-7-03-fifth_MainaxisAndCrossaxis/image-20220703223711849.png?raw=true)

<h5>그림1</h5>

# 2. Cross axis(Vertical)
<h5><span style="color:red">Corss axis(Vertical)는 align-items으로 설정가능하며, 수직(세로)축의 위치 설정의 기능</span>이 있습니다.</h5>

```python

align-items: center;

```
<h5>간단한 예로 align-items의 설정을 center로 설정을 하였을 시, <span style="color:red">수직축의 넓이에 따라 설정하는 것이 가능</span>합니다.<br>
(그림2 참조)</h5>
![image-20220703225327309](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-7-03-fifth_MainaxisAndCrossaxis/image-20220703225327309.png?raw=true)

<h5>그림2</h5>

<h5>다음 시간은 <span style="color:red">flex-direction에 대한 사용법</span>에 대해서 공부를 하는데 있어서 수평(Main axis)과 수직(Cross axis)의 개념이 중요하니 복습이 필수입니다.</h5>

