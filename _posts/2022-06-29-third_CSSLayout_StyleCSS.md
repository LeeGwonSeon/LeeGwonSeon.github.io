---
layout: single
title:  "How can make design?"
categories: coding
tag: [HTML, CSS, link, blog]
toc: true
author_profile: false
sidebar:
    nav: "docs"
---

<div class="notice">
<h2>first study list.</h2>
<ul>
    <li>1. html_box coding </li>
    <li>2. style_box design </li>
    <li>3. css link methot </li>
</ul>
</div>

# 1. html_box coding

```python

<body>
    <div class="box">1</div>
    <div class="box">2</div>
    <div class="box">3</div>
</body>
</html> 

```

body 안에 div로 class=box를 1, 2, 3  준비합니다. 이런식으로 리스트 작업을 할 때 div를 통한 class 설정으로 기초작업을 합니다.

# 2. style_box design

```python

.box {
    background: purple;
    width: 300px;
    height: 300px;
    display: inline-block;
    color: white;
}

```
class명을 활용하여 css에서 배경색깔과 width, height 및 dlsplay을 통해 나열의 방향을 inline-block 을 설정해 일직선으로 나열 가능하게 합니다.
여기서 inline과 inline-block의 차이점이 있는데 inline의 경우는 width, height의 제한이 없고, inline-block은 제한이 있는 box형태입니다. 

```python

.box:nth-child(2){
    margin-left: 35px;
}

.box:nth-child(3){
    margin-left: 35px;
} 

```

class명으로 3가지의 box를 준비하였습니다. 그것을 구분하기 위해
box뒤에 :nth-child(n)을 붙이고 원하는 자식을 설정하여 디자인을 따로 설정 할 수 있습니다.

# 3. css link methot

```python

<link rel="stylesheet" type="text/css" href="styles.css">

```

design을 하고 나서 가장 기본적으로 design 파일을 HTML file에 적용을 시키는데 있어서 위와 같이 link로 href="styles.css" file 설정을 하여, 
design을 적용하게 합니다.