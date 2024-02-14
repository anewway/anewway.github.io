---
layout: post
title:  "LeetCode 643. Maximum Average Subarray I"
date:   2024-02-14 19:53:04 +0800
categories: leetcode
---

# 題目：[643. Maximum Average Subarray I](https://leetcode.com/problems/maximum-average-subarray-i)

## 難度
Easy

## 簡述
在陣列中，以每 k 的長度為單位內逐一尋找，比較當前陣列視窗中的平均值，若比原先大，則替換為當前值，直到找到最大值為止。需考數量不足 k 的情況。

## 程式碼
TypeScript：
```typescript
function findMaxAverage(nums: number[], k: number): number {
    let max:number = - Number.MAX_SAFE_INTEGER;
    const windows:number[] = [];
    let currentSum = 0;
    for(const num of nums) {
        windows.push(num);
        currentSum += num;

        if(windows.length >= k) {
            const poped = windows.splice(0, windows.length - k);
            currentSum -= poped.shift() || 0;

            const average = currentSum / k;
            if(average > max) {
                max = average;
            }
        }
    }

    if(nums.length <= k) {
        const average = windows.reduce((a, b)=>a+b) / windows.length;
        max = average;
    }

    return max;
};
```