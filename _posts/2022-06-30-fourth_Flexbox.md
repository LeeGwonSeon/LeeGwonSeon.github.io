---
layout: single
title:  "What is Flexbox?"
categories: CSSLayout
tag: [HTML, CSS, Flexbox, blog]
toc: true
author_profile: false
sidebar:
    nav: "docs"
---

<div class="notice">
<h2>second study list.</h2>
<ul>
    <li>inline보다 발전된 flexbox</li>
    <p>전 시간의 정리한 내용에서 나온 inline-block의 기능보다 design에 편리한 flexbox의 사용법과 개념을 정리하였습니다.</p>
    <li>1. Flexbox? </li>
    <li>2. How can use it? </li>
    <li>3. Flexbox_Container and item </li>
</ul>
</div>


# 1. Flexbox?

flex box는 <span style= "color:red"> flex container(부모 요소)와 flex item(자식 요소)</span>로 구성됩니다. flexbox를 사용하려면 부모 요소에

<span style= "color:blue"> display: flex를 추가하면됩니다. flex 속성을 추가한 요소가 flex container가 되고, 그 자식 요소들이 flex item이 됩니다.</span> 

Flex의 핵심 아이디어는 화면 크기에 맞춰, 화면 안 아이템들의 넓이/높이를 가장 최적의 길이로 맞춰준다는 점입니다. 따라서 디바이스의 화면 크기에 따라 유동적으로 아이템들의 크기를 조정할 수 있다. 

또한 수평적으로만 배치되는 것이 원칙인 일반적인 레이아웃(block, inline..)과 달리, flexbox 레이아웃은 방향에 대해 조금 더 유연하다. 그리고 기존의 일반적인 레이아웃은 정적인 페이지에 대해서는 잘 작동하지만, 크거나 복잡한 어플리케이션(특히 방향 변경, 크기 조정, 늘리기, 축소 등) 에 대한 대응은 상대적으로 부족한 면이 있습니다.

<span style= "color:red"> Flexbox는 작은 크기의 레이아웃이나 모바일 디바이스에 적합</span>하고, 큰 스케일의 레이아웃을 원한다면 Grid 속성을 사용하는 것이 좋습니다.



# 2. How can use it?

![image-20220702140443772](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-06-30-fourth_Flexbox/image-20220702140443772.png?raw=true)

<span style= "color:red">flexbox는 flexbox container(부모개념) 안에 Item(자식 개념)으로 포함</span>된 것이 있는 것만 조작이 가능합니다. flexbox container을 설정하지 않은 상태에서 item만 조작은 안되니 flexbox container와 item 은 필수입니다.



# 3. Flexbox_Container and item

```python

body {
    display: flex;
}

```
flexbox container 의 선언 방법은 간단합니다. body(강의 할 때 흰 board판 개념)를 display로 설정을 합니다.
<br>
<br>

```python

.box {
    width: 200px;
    height: 200px;
    background-color: blueviolet;
    color: white;

```
flexbox container를 설정하게 되면 그 안의 item(box or 자식개념)을 조작가능하게 됩니다. (밑의 그림 참조)

![image-20220702144411681](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-06-30-fourth_Flexbox/image-20220702144411681.png?raw=true)
