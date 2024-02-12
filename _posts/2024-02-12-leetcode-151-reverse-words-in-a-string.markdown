---
layout: post
title:  "LeetCode 151. Reverse Words in a String"
date:   2024-02-12 19:53:04 +0800
categories: leetcode
---

# 題目：[151. Reverse Words in a String](https://leetcode.com/problems/reverse-words-in-a-string)

## 難度
Medium

## 簡述
移除句子中多餘的空格，並依空格將分單字區分出後反過來排列。

## 程式碼
TypeScript：
```typescript
function reverseWords(s: string): string {
    const words = s.split(' ').filter((word)=>word!=='');
    return words.reverse().join(' ');  
};
```