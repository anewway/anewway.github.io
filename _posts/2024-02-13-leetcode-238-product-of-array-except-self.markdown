---
layout: post
title:  "LeetCode 238. Product of Array Except Self"
date:   2024-02-12 19:53:04 +0800
categories: leetcode
---

# 題目：[238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self)

## 難度
Medium

## 簡述
由於要將當前 index 以外的所有值相乘，可從頭尾分別相乘後儲存數值，即可得出從頭或尾到該 index 為止的所有乘積，再將頭、尾的數值相乘，即可得出結果。

## 程式碼
TypeScript：
```typescript
function productExceptSelf(nums: number[]): number[] {
    const left:number[] = [];
    const right:number[] = [];
    const result:number[] = [];
    let tmp = 1;
    for(let i = 0; i < nums.length; i++) {
        left.push(tmp);
        tmp *= nums[i];
    }

    tmp = 1;
    for(let i = nums.length - 1; i >= 0; i--) {
        right.unshift(tmp);
        tmp *= nums[i];
    }

    for(let i = 0; i < nums.length; i++) {
       result.push(left[i] * right[i]);
    }

    return result;
};
```