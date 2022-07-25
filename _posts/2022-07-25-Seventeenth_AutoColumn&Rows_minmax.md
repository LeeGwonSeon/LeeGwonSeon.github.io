---
layout: single
title:  "Auto Column and Rows & Minmax"
categories: CSSLayout
tag: [CSS, CSSLayout, Grid, Auto Column, Auto Rows, fr, blog]
toc: true
author_profile: false
sidebar:
    nav: "docs"
---

<div class="notice">
<h2>Seventeenth_AutoColumn&Rows_minmax</h2>
<ul>
    <li>Auto Column and Rows & Minmax 개념 이해</li>
    <p>전 시간은 Grid의 Place Items와  Place content 에 대한 개념에 대해서 공부하였습니다. 이번 시간은 Auto Column and Rows & Minmax에 대한 개념을 정리하였습니다.</p>
    1. Auto Column and Rows
    2. Minmax
</ul>
</div>

# 1. Auto Column and Rows

<h5>이번 시간은 Auto Column과 Auto Rows 에 대한 개념을 설명하겠습니다.</h5>

```python

HTML
<body>
    <div class="grid">
        <div class="item">1</div>
        <div class="item">2</div>
        <div class="item">3</div>
        <div class="item">4</div>
        <div class="item">5</div>
        <div class="item">6</div>
        <div class="item">7</div>
        <div class="item">8</div>
        <div class="item">9</div>
        <div class="item">10</div>
        <div class="item">11</div>
        <div class="item">12</div>
        <div class="item">13</div>
        <div class="item">14</div>
        <div class="item">15</div>
        <div class="item">16</div>
        <div class="item">17</div>
        <div class="item">18</div>
        <div class="item">19</div>
        <div class="item">20</div>
        <div class="item">21</div>
        <div class="item">22</div>
        <div class="item">23</div>
        <div class="item">24</div>
        <div class="item">25</div>
        <div class="item">26</div>
        <div class="item">27</div>
        <div class="item">28</div>
        <div class="item">29</div>
        <div class="item">30</div>
        <div class="item">31</div>
        <div class="item">32</div>
        <div class="item">33</div>
        <div class="item">34</div>
        <div class="item">35</div>
        <div class="item">36</div>
        <div class="item">37</div>
        <div class="item">38</div>
        <div class="item">39</div>
        <div class="item">40</div>
        <div class="item">41</div>
        <div class="item">42</div>
        <div class="item">43</div>
        <div class="item">44</div>
        <div class="item">45</div>
        <div class="item">46</div>
        <div class="item">47</div>
        <div class="item">48</div>
        <div class="item">49</div>
        <div class="item">50</div>
    </div>
</body>

CSS
.grid{
    color: white;
    display: grid;
    gap: 5px;
    grid-template-columns: repeat(4, 100px);
    grid-template-rows: repeat(4, 100px);
  }

.item:nth-child(odd) {
    background-color: #2ecc71;
}

.item:nth-child(even) {
    background-color: #3498db;
  }

```

![image-20220725210010209](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-25-Seventeenth_AutoColumn%26Rows_minmax/image-20220725202211022.png?raw=true)

그림 1

<h5>위의 그림 1 기본설정을 한 상태에서 Auto Column과 Auto Rows에 대해 설명을 하겠습니다. </h5>


```python

HTML
<body>
    <div class="grid">
        <div class="item">1</div>
        <div class="item">2</div>
        <div class="item">3</div>
        <div class="item">4</div>
        <div class="item">5</div>
        <div class="item">6</div>
        <div class="item">7</div>
        <div class="item">8</div>
        <div class="item">9</div>
        <div class="item">10</div>
        <div class="item">11</div>
        <div class="item">12</div>
        <div class="item">13</div>
        <div class="item">14</div>
        <div class="item">15</div>
        <div class="item">16</div>
        <div class="item">17</div>
        <div class="item">18</div>
        <div class="item">19</div>
        <div class="item">20</div>
        <div class="item">21</div>
        <div class="item">22</div>
        <div class="item">23</div>
        <div class="item">24</div>
        <div class="item">25</div>
        <div class="item">26</div>
        <div class="item">27</div>
        <div class="item">28</div>
        <div class="item">29</div>
        <div class="item">30</div>
        <div class="item">31</div>
        <div class="item">32</div>
        <div class="item">33</div>
        <div class="item">34</div>
        <div class="item">35</div>
        <div class="item">36</div>
        <div class="item">37</div>
        <div class="item">38</div>
        <div class="item">39</div>
        <div class="item">40</div>
        <div class="item">41</div>
        <div class="item">42</div>
        <div class="item">43</div>
        <div class="item">44</div>
        <div class="item">45</div>
        <div class="item">46</div>
        <div class="item">47</div>
        <div class="item">48</div>
        <div class="item">49</div>
        <div class="item">50</div>
    </div>
</body>

CSS
.grid{
    color: white;
    display: grid;
    gap: 5px;
    grid-template-columns: repeat(4, 100px);
    grid-template-rows: repeat(4, 100px);
    grid-auto-flow: rows;
    grid-auto-rows: 100px;
  }

.item:nth-child(odd) {
    background-color: #2ecc71;
}

.item:nth-child(even) {
    background-color: #3498db;
  }

```

<h5>위와 같이 CSS 영역에서 <span style="color:red">grid-auto-flow로 rows(수직)와 columns(수평)으로 설정이 가능</span>한데, 기본 설정으로는 rows 방향으로 되어 있기 때문에 flow에서 rows를 설정할 경우는 없이도 가능합니다. 그리고 <span style="color:red">grid-template-rows에서 repeat 제한보다 child가 많을 경우 grid auto-rows로 px 를 설정하면, 많은 경우에도 그림 2처럼 자동으로 설정</span>이 가능합니다.</h5>

![image-20220725210010209](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-25-Seventeenth_AutoColumn%26Rows_minmax/image-20220725210010209.png?raw=true)

그림 2

```python

CSS
.grid{
    color: white;
    display: grid;
    gap: 5px;
    grid-template-columns: repeat(10, 100px);
    grid-template-rows: repeat(4, 100px);
    grid-auto-flow: column;
    grid-auto-columns: 100px;
  }

.item:nth-child(odd) {
    background-color: #2ecc71;
}

.item:nth-child(even) {
    background-color: #3498db;
  }

```
<h5>column(수직)방향도 <span style="color:red">grid-auto-flow에서 column으로 설정 가능하며, column도 row와 마찬가지 child가 지정한것보다 많을 경우 그림 3 처럼 화면이 표시가 됩니다. 그것을 grid-auto-column에서 px을 설정해주면 그림 4 처럼 설정이 가능</span>합니다. 이 방법대로라면 달력이나 사진을 설정할 때 효과 적일 것입니다. </h5>

![image-20220725211541312](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-25-Seventeenth_AutoColumn%26Rows_minmax/image-20220725211541312.png?raw=true)

그림 3

![image-20220725211706512](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-25-Seventeenth_AutoColumn%26Rows_minmax/image-20220725211706512.png?raw=true)

그림 4

# 2. Minmax
<h5>minmax는 child의 최소값과 최대값을 설정 가능한 기능을 가지고 있습니다.</h5>

```python

HTML
<body>
    <div class="grid">
        <div class="item">1</div>
        <div class="item">2</div>
        <div class="item">3</div>
        <div class="item">4</div>
        <div class="item">1</div>
        <div class="item">2</div>
        <div class="item">3</div>
        <div class="item">4</div>
        <div class="item">1</div>
        <div class="item">2</div>
        <div class="item">3</div>
        <div class="item">4</div>
        <div class="item">1</div>
        <div class="item">2</div>
        <div class="item">3</div>
        <div class="item">4</div>
    </div>
</body>

CSS
.grid{
    color: white;
    display: grid;
    gap: 5px;
    grid-template-columns: repeat(5, 1fr);
    grid-template-rows: repeat(4, 100px);
    columns: 100px;
  }

.item:nth-child(odd) {
    background-color: #2ecc71;
}

.item:nth-child(even) {
    background-color: #3498db;
  }

```

<h5>위처러머 grid-template-column에서 repeat으로 제한을 정하지 않은 1fr로 하였을 경우 그림 5 처럼 전체화면에서 child가 화면 크기에 맞게 늘어난 것을 확인할 수 있습니다.</h5>

![image-20220725213020572](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-25-Seventeenth_AutoColumn%26Rows_minmax/image-20220725213020572.png?raw=true)

그림 5

<h5>화면의 크기가 줄었다가 크게 해도 child의 크기의 제한을 두는 것이 minmax의 기능입니다. </h5>

```python

HTML
<body>
    <div class="grid">
        <div class="item">1</div>
        <div class="item">2</div>
        <div class="item">3</div>
        <div class="item">4</div>
        <div class="item">1</div>
        <div class="item">2</div>
        <div class="item">3</div>
        <div class="item">4</div>
        <div class="item">1</div>
        <div class="item">2</div>
        <div class="item">3</div>
        <div class="item">4</div>
        <div class="item">1</div>
        <div class="item">2</div>
        <div class="item">3</div>
        <div class="item">4</div>
    </div>
</body>

CSS
.grid{
    color: white;
    display: grid;
    gap: 5px;
    grid-template-columns: repeat(5, minmax(100px, 150px));
    grid-template-rows: repeat(4, 100px);
    columns: 100px;
  }

.item:nth-child(odd) {
    background-color: #2ecc71;
}

.item:nth-child(even) {
    background-color: #3498db;
  }

```

<h5><span style="color:red">minmax는 첫 번째 칸에 최소값을 설정하며, 두 번째 칸에 최대값을 설정</span>할 수 있습니다. 위의 설정을 그림 6 에서 확인할 수 있듯이 <span style="color:red">minmax에서 최소값을 100px 최대값을 150px으로 설정</span>하였기에 그림 6 과 같은 결과가 나왔습니다. </h5>

![image-20220725213649116](https://github.com/LeeGwonSeon/LeeGwonSeon.github.io/blob/master/imeages/2022-07-25-Seventeenth_AutoColumn%26Rows_minmax/image-20220725213649116.png?raw=true)

그림 6