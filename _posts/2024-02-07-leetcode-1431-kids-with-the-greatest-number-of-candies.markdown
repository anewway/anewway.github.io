---
layout: post
title:  "LeetCode 1431. Kids With the Greatest Number of Candies"
date:   2024-02-07 19:53:04 +0800
categories: leetcode
---

# 題目：[1431. Kids With the Greatest Number of Candies](https://leetcode.com/problems/kids-with-the-greatest-number-of-candies)

## 難度
Easy

## 簡述
先找出最大值當基準，再逐一做判斷。

## 程式碼
TypeScript：
```typescript
function kidsWithCandies(candies: number[], extraCandies: number): boolean[] {
    let oldMax = 0;
    for(const candy of candies) {
        if(candy > oldMax) {
            oldMax = candy;
        }
    }

    const result:boolean[] = [];
    for(const candy of candies) {
        if(candy + extraCandies >= oldMax) {
            result.push(true);
            continue;
        }

        result.push(false);
    }

    return result;
};
```
