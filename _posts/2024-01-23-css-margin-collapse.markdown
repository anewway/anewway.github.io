---
layout: post
title:  "CSS margin collapse"
date:   2024-01-23 19:53:04 +0800
categories: css
---


## 說明
在同層的區塊中，會使用 margin 設定來保持元素之間的間距，在調整垂直間距(top/bottom)時，總是會遇到間距重疊(margin collapse)的問題，導致間距較小的區塊 margin 被吃掉，可將外層區塊設定為 grid layout 來避免此狀況。



## 程式碼：[線上範例](https://codepen.io/anewway/pen/poYrWBy){:target="_blank"}

HTML
```html
<div class="container flow">
  Flow layout
  <div class="block bottom">block 1</div>
  <div class="block top">block 2</div>  
</div>

<div class="container grid">
  Grid layout
  <div class="block bottom">block 1</div>
  <div class="block top">block 2</div>  
</div>
```

CSS
```css
.container {
  background: pink;
  margin: 20px;
}
.grid {
  display: grid;
}
.block {
  background: #96E9C6;
  width: 200px;
  height: 100px;
  padding: 1px;
  margin: 10px;
}
.bottom {
  margin-bottom: 40px;
}
.top {
  margin-top: 30px;
}
```
