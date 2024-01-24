---
layout: post
title:  "CSS text indent"
date:   2024-01-24 19:53:04 +0800
categories: css
---


## 說明
段落中第一行字首含有特殊字元(或圖案)，而剩餘文字段落需第一行其餘文字對齊時，可使用 text-indent 來達成。


## 程式碼：[線上範例](https://codepen.io/anewway/pen/PoLJPKY){:target="_blank"}

HTML
```html

<h1>Normal</h1>
<p class="normal">
* Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse eu
  venenatis quam. Vivamus euismod eleifend metus vitae pharetra. In vel tempor
  metus. Donec dapibus feugiat euismod. Vivamus interdum tellus dolor. Vivamus
  blandit eros et imperdiet auctor. Mauris sapien nunc, condimentum a efficitur
  non, elementum ac sapien. Cras consequat turpis non augue ullamcorper, sit
  amet porttitor dui interdum.
</p>
<h1>Text Indent</h1>
<p class="indent">
* Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse eu
  venenatis quam. Vivamus euismod eleifend metus vitae pharetra. In vel tempor
  metus. Donec dapibus feugiat euismod. Vivamus interdum tellus dolor. Vivamus
  blandit eros et imperdiet auctor. Mauris sapien nunc, condimentum a efficitur
  non, elementum ac sapien. Cras consequat turpis non augue ullamcorper, sit
  amet porttitor dui interdum.
</p>
```

CSS
```css
p {
  background: #99BC85;
  padding: 20px;
  width: 800px;
}

.indent {
  text-indent: -12px;
}
```
