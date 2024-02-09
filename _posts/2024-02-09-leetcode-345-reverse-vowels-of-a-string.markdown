---
layout: post
title:  "LeetCode 345. Reverse Vowels of a String"
date:   2024-02-09 19:53:04 +0800
categories: leetcode
---

# 題目：[345. Reverse Vowels of a String](https://leetcode.com/problems/reverse-vowels-of-a-string)

## 難度
Easy

## 簡述
集中屬於母音的字元，從輸入的字串提取母音出來另外存，並將原本的位置設成空值，收集完所有的母音之後，從最後一個空值開始倒回去填入那些母音即可。

## 程式碼
TypeScript：
```typescript
function reverseVowels(s: string): string {
    const alphabets = [...s];
    const EMPTY_VALUE = '*';
    const VOWEL_STRING = 'aeiou';
    const vowels:string[] = [...(VOWEL_STRING.toUpperCase()), ...(VOWEL_STRING.toLowerCase())];
    const candidates:string[] = [];
    for(let i = 0; i < alphabets.length; i++) {
        const alphabet = alphabets[i];
        if(vowels.includes(alphabet)) {
            candidates.push(alphabet);
            alphabets[i] = EMPTY_VALUE;
        }
    }

    for(let i = 0; i < alphabets.length; i++) {
        if(alphabets[i] !== EMPTY_VALUE )continue;
        const candidate = candidates.pop();
        alphabets[i] = candidate;
    }

    return alphabets.join('');
};
```
