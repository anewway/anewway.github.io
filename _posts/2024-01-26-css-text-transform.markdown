---
layout: post
title:  "CSS text transform"
date:   2024-01-26 19:53:04 +0800
categories: css
---


## 說明
使用 `text-transform` 來控制字母的大小寫。

## 程式碼：[線上範例](https://codepen.io/anewway/pen/bGZYgob){:target="_blank"}

HTML
```html
<div class="normal">
  <h1>Normal</h1>
  <p>The only thing we have to fear is fear itself.</p>
</div>

<div class="uppercase">
  <h1>Uppercase</h1>
  <p>The only thing we have to fear is fear itself.</p>
</div>

<div class="lowercase">
  <h1>Lowercase</h1>
  <p>The only thing we have to fear is fear itself.</p>
</div>

<div class="capitalize">
  <h1>Capitalize</h1>
  <p>The only thing we have to fear is fear itself.</p>
</div>
```

CSS
```css
.uppercase {
  text-transform: uppercase;
}
.lowercase {
  text-transform: lowercase;
}
.capitalize {
  text-transform: capitalize;
}
```
