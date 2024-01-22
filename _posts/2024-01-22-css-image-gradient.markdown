---
layout: post
title:  "CSS 使用 linear-gradient 幫圖片加上漸層背景"
date:   2024-01-22 19:53:04 +0800
categories: jekyll update
---


## 說明
如果想在現有圖片加上其他背景色，除了新增一個 `div` 元素覆蓋在原本的圖片以外，還可以使用 CSS `linear-gradient` 同時將圖片與背景設定完成。

## 程式碼：[線上範例](https://codepen.io/anewway/pen/vYPZPvN){:target="_blank"}

HTML
```html
<div class="background cover"></div>
```

CSS
```css
.background {
    width: 400px;
    height: 250px;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center bottom;
}

.cover {
    background-image: linear-gradient(0deg, rgba(255, 255, 255, 0.5), rgba(255, 255, 255, 0.1)), url('https://images.unsplash.com/photo-1683009427500-71296178737f?q=80&w=2071&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDF8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D');
}
```
