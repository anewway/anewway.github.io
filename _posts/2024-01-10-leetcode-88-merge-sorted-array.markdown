---
layout: post
title:  "LeetCode 88. Merge Sorted Array"
date:   2024-01-10 19:53:04 +0800
categories: jekyll update
---

# 題目：[88. Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/description/)

## 類型
Top Interview 150

## 難度
Easy

## 簡述
給定兩組陣列，將第二組陣列加到第一組陣列中，並從小到大排序。

## 解法
移除第一組陣列中佔位用的數字，加入第二組陣列的數字，把所有數字重新排序。

TypeScript 程式碼：
```typescript
function merge(nums1: number[], m: number, nums2: number[], n: number): void {
    for(let i = nums1.length; i >= 0; i--) {
        const number = nums1[i];
        if(number === 0 && n > 0) { // 移除佔位用的數字
            nums1.splice(i, 1);
            i++; // 避免陣列長度改變後索引錯位
            n--; // 計算佔位數字的數量
        }
    }

    for(let i = 0; i < nums2.length; i++) {
        const number = nums2[i];
        nums1.push(number); // 加入第二組陣列的數字
    }

    nums1.sort(function (a, b) { // 所有數字重新排序
        return a - b;
    });
};
```
