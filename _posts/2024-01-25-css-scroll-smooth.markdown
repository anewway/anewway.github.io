---
layout: post
title:  "CSS scroll smooth"
date:   2024-01-25 19:53:04 +0800
categories: css
---


## 說明
使用 scroll smooth 讓網頁錨點移動更滑順。

## 程式碼：[線上範例](https://codepen.io/anewway/pen/zYbEMBz){:target="_blank"}

HTML
```html
<nav>
  <a href="#anchor-1" >anchor1</a>
  <a href="#anchor-2" >anchor2</a>
  <a href="#anchor-3" >anchor3</a>
</nav>
<main>
  <div id="anchor-1">anchor 1</div>
  <div id="anchor-2">anchor 2</div>
  <div id="anchor-3">anchor 3</div>  
</main>
```

CSS
```css
* {
  scroll-behavior: smooth;
}
nav {
  margin: 20px;
}
div {
  margin: 20px;
  background: #17deb8;
  width: 600px;
  height: 100vh;
}
```
