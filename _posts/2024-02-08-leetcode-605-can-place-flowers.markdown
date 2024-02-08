---
layout: post
title:  "LeetCode 605. Can Place Flowers"
date:   2024-02-08 19:53:04 +0800
categories: leetcode
---

# 題目：[605. Can Place Flowers](https://leetcode.com/problems/can-place-flowers)

## 難度
Easy

## 簡述
左中右分別判斷，如果可以放就減少 n 的數量，直到不夠放為止。

## 程式碼
TypeScript：
```typescript
function canPlaceFlowers(flowerbed: number[], n: number): boolean {
    for(let i = 0; i < flowerbed.length; i++) {
        if(flowerbed[i] === 1) continue;
        if(flowerbed[i-1] === 1) continue;
        if(flowerbed[i+1] === 1) continue;

        if(n <= 0) break;

        flowerbed[i] = 1;
        n--;
    }

    return n === 0;
};
```
