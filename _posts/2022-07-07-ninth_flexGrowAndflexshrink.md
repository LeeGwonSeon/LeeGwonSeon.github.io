---
layout: single
title:  "flex-grow와 flex-shrink"
categories: CSSLayout
tag: [CSS, CSSLayout, Flexbox, flex-grow, flex-shrink,  blog]
toc: true
author_profile: false
sidebar:
    nav: "docs"
---

<div class="notice">
<h2>Nineth study list.</h2>
<ul>
    <li>flex-grow와 flex-shrink 개념 이해</li>
    <p>전 시간은 wrap, nowrap, reverse, align-content에 대한 개념에 대해서 공부하였습니다. 이번 시간은 flex-grow와 flex-shrink에 대한 개념을 정리하였습니다.</p>
    <li>1. flex-shrink</li>
    <li>2. flex-grow</li>
</ul>
</div>

# 1. flex-shrink
<h5>flex-shrink는 element 행동을 부여하는 기능입니다. 웹의 화면을 줄였을 때, flex-shrink로 설정한 child가 더 작아지게 할 수 있습니다. 주로 반응형 페이지를 만들 때 사용되는데 iPhone등과 같은 곳에 많이 사용됩니다.</h5>

```python

.child:nth-child(2) {
    background-color: black;
}


```


```python

.child:nth-child(2) {
    background-color: black;
    flex-shrink: 1;
}


```

<h5>child에서 flex-shrink을 설정전과 설정 후에 대해 차이가 있지만 flex-shrink의 설정을 1로 하였을 경우, 기본 설정과 차이가 없기 때문에 그림 1의 결과가 나타납니다.</h5>

![image-20220707211858421](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-07-ninth_flexGrowAndflexshrink/image-20220707211858421.png?raw=true)


```python

.child:nth-child(2) {
    background-color: black;
    flex-shrink: 2;
}


```
<h5>child2에서 flex-shrink을 설정을 2로 한 후 웹화면을 그림3 처럼 축소를 하게 될 경우에 child2의 크기는 다른 child보다 작아지는 것을 볼 수 있습니다.</h5>

![image-20220707212801319](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-07-ninth_flexGrowAndflexshrink/image-20220707212801319.png?raw=true)

그림 3



```python

.child:nth-child(2) {
    background-color: black;
    flex-shrink: 3;
}

.child:nth-child(3) {
    flex-shrink: 2;
}

```

<h5>이처럼 flex-shrink를 설정 후 화면을 줄였을 때, 중요한 것 외에는 작게 하는 반응형의 페이지를 만드는 데 도움이 됩니다.(그림4 참조) </h5>

![image-20220707213610021](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-07-ninth_flexGrowAndflexshrink/image-20220707213610021.png?raw=true)

그림4

# 2. flex-grow
<h5>flex-grow또한 element 행동을 부여하는 기능입니다. flex-shrink는 웹의 화면을 줄였을 때, child가 더 작아지게 할 수 있고 반대로 flex-grow를 설정하여 화면을 크게 했을 때 child의 크기를 더 크게 하는 기능입니다.</h5>


```python

.child:nth-child(2) {
    background-color: black;
    flex-grow: 2;
}

```

<h5>child2에 flex-grow를 2로 설정을 한 후 화면을 크게 늘리게 되면 line의 빈 공간을 안보이게 늘리게 되어, 그림5 의 화면처럼 가능하게 됩니다.</h5>

![image-20220707214732471](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-07-ninth_flexGrowAndflexshrink/image-20220707214732471.png?raw=true)

그림 5

```python

.child:nth-child(2) {
    background-color: black;
    flex-grow: 2;
}

.child:nth-child(3) {
    flex-grow: 1;
}

```

<h5>위와 같이 child2, child1을 flex-grow으로 설정을 하게 되면 비율에 맞게 크기가 커지게 됩니다. (그림 6 참조)</h5>

![image-20220707215130610](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-07-ninth_flexGrowAndflexshrink/image-20220707215130610.png?raw=true)

그림 6
