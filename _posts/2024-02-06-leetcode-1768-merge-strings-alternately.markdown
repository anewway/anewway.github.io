---
layout: post
title:  "LeetCode 1768. Merge Strings Alternately"
date:   2024-02-06 19:53:04 +0800
categories: leetcode
---

# 題目：[1768. Merge Strings Alternately](https://leetcode.com/problems/merge-strings-alternately)

## 難度
Easy

## 簡述
分別建立 2 個索引值，照順序把 2 組字串的值加入新的陣列中。

## 程式碼
TypeScript：
```typescript
function mergeAlternately(word1: string, word2: string): string {
    let total = word1.length + word2.length; 
    let index1 = 0; // 記錄第 1 組字元的索引值
    let index2 = 0; // 記錄第 2 組字元的索引值
    const concates:string[] = [];
    while(total--) {
        const alphabet1 = word1[index1++]; // 第 1 組字元個別的值
        const alphabet2 = word2[index2++]; // 第 2 組字元個別的值

        if(alphabet1 !== undefined) { // 如果有值，就加到結果的陣列中
            concates.push(alphabet1);
        }

        if(alphabet2 !== undefined) { // 如果有值，就加到結果的陣列中
            concates.push(alphabet2);
        }
    }

    return concates.join('');
};
```
