---
layout: single
title:  "Auto-fit Auto-fill & Min-content Max-content"
categories: CSSLayout
tag: [CSS, CSSLayout, Grid, Auto-fit, Auto-fill, content, Min-content, Max-content, fr, blog]
toc: true
author_profile: false
sidebar:
    nav: "docs"
---

<div class="notice">
<h2>Eighteenth_Auto-fit Auto-fill & Min-content Max-content study list.</h2>
<ul>
    <li>Auto-fit Auto-fill & Min-content Max-content 개념 이해</li>
    <p>전 시간은 Grid의 Place Items와  Place content에 대한 개념에 대해서 공부하였습니다. 이번 시간은 Grid의 Auto-fit Auto-fill 과 Min-content Max-content 정리하였습니다.</p>
    1. Auto-fit Auto-fill
    2. Min-content Max-content
</ul>
</div>

# 1. Auto-fit Auto-fill

<h5>이번 시간은 Auto-fit과 Auto-fill 에 대한 개념을 설명하겠습니다.</h5>

```python

HTML
auto-fill
    <div class="grid">
      <div class="item">1</div>
      <div class="item">2</div>
      <div class="item">3</div>
      <div class="item">4</div>
      <div class="item">5</div>
      <div class="item">6</div>
    </div>
    auto-fit
    <div class="grid">
      <div class="item">1</div>
      <div class="item">2</div>
      <div class="item">3</div>
      <div class="item">4</div>
      <div class="item">5</div>
      <div class="item">6</div>
    </div>

CSS
.grid {
    color: white;
    display: grid;
    gap: 5px;
    grid-auto-rows: 100px;
    margin-bottom: 30px;
  }
  
  .item:nth-child(odd) {
    background-color: #2ecc71;
  }
  
  .item:nth-child(even) {
    background-color: #3498db;
  }
  
  .grid:first-child {
    grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
  }
  
  .grid:last-child {
    grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
  }

```

<h5>위와 같이 auto-fit과 auto-fill를 이해하기 위해 HTML에서 영역을 나눠서 그림 1 처럼 표현하였습니다. auto-fit과 auto-fill을 간단히 설명하면, <span style="color:red">auto-fill은 column을 만들어 주는 일을 합니다. 즉, 해당 row에서 column이 있는 개수만큼 추가를 해줍니다. auto-fit은 현재 있는 child를 row의 화면 크기에 맞게 늘려서 채워줍니다.</span></h5>

![image-20220726192928894](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-26-Eighteenth_Auto-fit%20Auto-fill%20%26%20Min-content%20Max-content/image-20220726192928894.png?raw=true)

그림 1

<h5>웹 화면을 줄였을 때는 auto-fit과 auto-fill이 같은 크기로 보여서 구분하기 어렵지만 그림 2 처럼 전체화면을 하였을 때, 위의 설명처럼 차이가 있는 것을 알 수 있습니다.</h5>

![image-20220726193227365](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-26-Eighteenth_Auto-fit%20Auto-fill%20%26%20Min-content%20Max-content/image-20220726193227365.png?raw=true)

그림 2

# 2. Min-content Max-content

<h5>CSS Layout의 기초공부를 하면서 content 디자인에 대한 궁금함이 있기도 하여 공부를 하는데 있어서 min-content와 max-content를 사용하여 반응형 페이지를 만들어 지는것을 보고 매력을 느껴 개념을 정리하였습니다.</h5>

<h5>min-content와 max-content을 간단히 정리하자면, <span style="color:red">min-content는 box를 만든다고 했을 때 content가 작아질 수 있을 만큼 작아지게 만드는 것이며, max-content는 box를 만든다고 했을 때 content가 필요한 만큼 크게 만드는 것</span>입니다.</h5>

```python

HTML
<body>
    <div class="grid">
        <div class="item">This is a very long text</div>
        <div class="item">This is a very longer longer long text</div>
        <div class="item">This is a text</div>
        <div class="item">
          Not long at all, or maybe, who knows? Maybe you know, love you.
        </div>
  
        <div class="item">This is a very longer long text</div>
        <div class="item">This is a very longer long text</div>
        <div class="item">This is a very longer long text</div>
        <div class="item">This is a very longer long text</div>
      </div>
</body>

CSS
.grid {
    color: white;
    display: grid;
    gap: 5px;
    grid-template-columns: min-content max-content;
    grid-auto-rows: 100px;
    margin-bottom: 30px;
  }
  
  .item:nth-child(odd) {
    background-color: #2ecc71;
  }
  
  .item:nth-child(even) {
    background-color: #3498db;
  }

```
<h5>grid-template-columns의 설정에서 min-content와  max-content가 설정이 되어 있는 것을 보실 수 있습니다. 위와 같이 설정을 하여 웹화면을 크게 하였을 때, 그림 3에서의 결과를 참고하시기 바랍니다.</h5>

![image-20220726194613780](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-26-Eighteenth_Auto-fit%20Auto-fill%20%26%20Min-content%20Max-content/image-20220726194613780.png?raw=true)

그림 3