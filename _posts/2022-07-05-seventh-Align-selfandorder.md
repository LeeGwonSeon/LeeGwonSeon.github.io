---
layout: single
title:  "Align-self & order"
categories: CSSLayout
tag: [CSS, CSSLayout, Flexbox, align-self, order, blog]
toc: true
author_profile: false
sidebar:
    nav: "docs"
---

<div class="notice">
<h2>Seventh study list.</h2>
<ul>
    <li>align-self와 order</li>
    <p>전 시간은 Flex-direction의 Column(세로)과 Row(가로)에 대한 개념에 대해서 공부하였습니다. 이번 시간은 algin-self와 order에 대한 개념을 정리하였습니다.</p>
    <li>1. align-self</li>
    <li>2. order</li>
</ul>
</div>

# 1. align-self
<h5>align-self는 오직 item에서만 적용이 가능하며, Cross axis 방향으로만 수정이 가능합니다.</h5>

```python

.child:nth-child(2) {
    align-self: center;
}

.child:nth-child(3) {
    align-self: flex-end;

```

<h5>이해를 돕기 위해 item명을 [child]로 표현하였습니다. 위의 내용처럼 <span style="color:red">child를 수정할 때에는 (item명):nth-child(n)을 지정</span>한 후에 설정이 가능해집니다.</h5>

![image-20220705193839723](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-05-seventh-Align-selfandorder/image-20220705193839723.png?raw=true)

<h6>그림1</h6>

# 2. order
<h5>order는 align-self와 마찬가지로 item(child)만 설정이 가능하며, HTML에서 바꿀 수 없는 것이 있을 때 child를 지정하여 설정 가능합니다.</h5>


```python

.child:nth-child(2) {
    order: 1;
}

```

<h5>2번째 child를 설정하여 <span style="color:red">order:1로 설정을 하게 되면 2번째 child가 3번째로 이동</span>을 하게 되고, child3번은 2번째 자리로 위치가 바뀝니다.</h5>

![image-20220705195159521](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-05-seventh-Align-selfandorder/image-20220705195159521.png?raw=true)



<h5>child2가 3번째로 위치가 바뀌고, child3은 두번째로 위치가 바뀌는 것은 <span style="color:red">child2의 order를 1로 설정되어 있고, child1, child3는 order가 0으로 되어 있기 때문</span>에 위와 같은 설정이 가능합니다.</h5>

```python

.child:nth-child(1) {
    order: 2;
}

.child:nth-child(2) {
    order: 3;

```

![image-20220705201618402](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-05-seventh-Align-selfandorder/image-20220705201618402.png?raw=true)

<h5>2번째 예로<span style="color:red">child2, child3의 order를 1로 설정되어 있고, child1는 order가 0으로 되어 있기 때문</span>에 위와 같은 설정이 가능합니다. 또한 이러한 상태에서flex-direction의 column과 align-silf에서 center를 설정하여 위치도 변경하여 꾸미는 것이 가능하니 디자인에 있어서 멋지게 꾸밀 수 있습니다.</h5>

```python
.father {
    display: flex;
    justify-content: space-around;
    /* Main Axis */
    height: 100vh;
    flex-direction: column;
}

.child:nth-child(1) {
    order: 2;
    align-self: center;
}

```

![image-20220705202230684](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-05-seventh-Align-selfandorder/image-20220705202230684.png?raw=true)





