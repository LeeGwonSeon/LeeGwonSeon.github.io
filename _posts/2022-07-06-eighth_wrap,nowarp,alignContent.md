---
layout: single
title:  "wrap, nowrap, reverse, align-content"
categories: CSSLayout
tag: [CSS, CSSLayout, Flexbox, wrap, nowrap, reverse, align-content, blog]
toc: true
author_profile: false
sidebar:
    nav: "docs"
---

<div class="notice">
<h2>Eighth study list.</h2>
<ul>
    <li>wrap, nowrap, reverse, align-content의 개념 이해</li>
    <p>전 시간은 algin-self와 order에 대한 개념에 대해서 공부하였습니다. 이번 시간은 wrap, nowrap, reverse, align-content에 대한 개념을 정리하였습니다.</p>
    <li>1. wrap and nowrap</li>
    <li>2. reverse</li>
    <li>3. align-content</li>
</ul>
</div>

# 1. wrap and nowrap
wrap과 nowrap을 간단하게 설명하자면 width을 무시하게 하거나
width크기를 유지하게 하는 방법입니다. 

```python

.child {
    width: 200px;
    height: 200px;
    background: purple;
    color: white;
    font-size: 50px;
}

```

<h5>child의 width(너비)와 height를 설정해놓은 상태에서 flexbox를 지정하게 되면 <span style="color:blue">flexbox item들 한 line으로만 존재하려 하기 때문에  width을 설정을 하더라도 한 line에 구겨넣게 됩니다.</span></h5>

![image-20220706204747683](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-06-eighth_wrap%2Cnowarp%2CalignContent/image-20220706204747683.png?raw=true)

```python

.child {
    width: 200px;
    height: 200px;
    background: purple;
    color: white;
    font-size: 50px;
    display: flex;
    justify-content: center;
    align-item: center;
}

```

<h5>또한, child에서 <span style="color:red">flexbox를 설정한 후 maix axis와 cross axis를 지정하면 위치설정이 가능</span>합니다. 예를 들어서 main axis와 cross axis를 center로 설정하였을 때입니다.</h5>

![image-20220706205305822](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-06-eighth_wrap%2Cnowarp%2CalignContent/image-20220706205305822.png?raw=true)

<h5>이처럼 item(child)의 위치를 가운데로 오게 할 수 있습니다.</h5>

```python

.father {
    display: flex;
    justify-content: space-around;
    height: 100vh;
    flex-wrap: nowrap;
}

```

<h5>이 상태에서 flex-wrap을 nowrap으로 설정을 하게 되면, <span style="color:red">무슨 짓을 하더라도 이 element들 즉, item들은 같은 줄에 있으라고 설정을 하는 것</span>입니다. 그렇기 때문에 처음에 flexbox를 설정하여 한 line에 구겨넣은 것처럼 변화가 생기지 않습니다.</h5>

![image-20220706205305822](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-06-eighth_wrap%2Cnowarp%2CalignContent/image-20220706205305822.png?raw=true)

```python

.father {
    display: flex;
    justify-content: space-around;
    height: 100vh;
    flex-wrap: wrap;
}

```

<h5>하지만 flex-wrap의 설정을 nowrap에서 wrap으로 바꾸게 되면 <span style="color:red">child의 width 무시하지 말고, 그 크기를 유지하라고 설정</span>하는 것이기 때문에 밑의 결과가 나타나게 됩니다.</h5>

![image-20220706210813431](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-06-eighth_wrap%2Cnowarp%2CalignContent/image-20220706210813431.png?raw=true)

# 2. reverse
<h5>reverse는 현재 사용하고 있는 item(child)를 역방향으로 나타내라고 하는 설정입니다.</h5>

```python

.father {
    display: flex;
    flex-direction: row-reverse;
    justify-content: space-around;
    height: 100vh;
}

```

<h5>flex-direction에서 <span style="color:red">row-reverse로 설정을 하게 되면 1부터 7의 순서에서 7에서 1 순서로 역방향이 됩니다.</span>(column-reverse로 cross axis에서도 역방향이 가능합니다.)
</h5>

![image-20220706212029715](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-06-eighth_wrap%2Cnowarp%2CalignContent/image-20220706212029715.png?raw=true)

![image-20220706212121626](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-06-eighth_wrap%2Cnowarp%2CalignContent/image-20220706212121626.png?raw=true)

<h5>또한, reverse는 flex-wrap에서도 설정이 가능합니다. 예를 들어 밑의 내용을 입력하게 되면 그림1 처럼 설정이 가능합니다.</h5>

```python

.father {
    display: flex;
    justify-content: space-around;
    height: 100vh;
    flex-wrap: wrap-reverse;
}

```

![image-20220706213018787](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-06-eighth_wrap%2Cnowarp%2CalignContent/image-20220706213018787.png?raw=true)

그림1

<h5>그림1 을 보게 되면 6번과 7번의 child가 역방향인 위로 나타나는 것을 확인할 수 있습니다.</h5>

# 3. align-content
<h5>align-content는 wrap으로 지정한 item(child)가 화면이 작아 졌을 때 자동으로 줄바꿈을 한 line의 간격의 위치의 설정을 가능하게 합니다.</h5>

```python

.father {
    display: flex;
    justify-content: space-around;
    align-content: space-around;
    height: 120vh;
    flex-wrap: wrap;
}

```

<h5>height의 안에서 align-content의 설정을 하게 되면 child의 위치가 그림2와 같이 설정이 가능하게 됩니다. </h5>

![image-20220706214025256](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-06-eighth_wrap%2Cnowarp%2CalignContent/image-20220706214025256.png?raw=true)

그림2