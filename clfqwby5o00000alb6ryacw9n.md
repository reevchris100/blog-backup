---
title: "Valid Anagram"
seoTitle: "Valid Anagram - Leetcode Coding solution"
seoDescription: "Valid Anagram - Leetcode Coding solution to find if a string is a valid anagram of another."
datePublished: Mon Mar 27 2023 14:00:06 GMT+0000 (Coordinated Universal Time)
cuid: clfqwby5o00000alb6ryacw9n
slug: valid-anagram
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679925099335/4514e8f3-d786-4e1c-90ab-efb8de7a45be.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1679925539486/534bb36e-f97c-4b13-8f89-5c09289e9347.jpeg
tags: coding, leetcode, anagram, valid, valid-anagrams

---

### Problem

Given two strings, return true if one of them is an anagram of another. This is similar to the Leetcode Problem - [Valid Anagram](https://leetcode.com/problems/valid-anagram/)

### Approach

The approach would be creating a character array containing 26 alphabets as characters. We then iterate both strings, add characters from one of the strings and remove them using another string at the same index. If the count of each character is equal to 0, it is a valid anagram.

```java
class Solution {
    public boolean isAnagram(String s, String t) {
         if(s.length()!=t.length()){
            return false;
        }
        int[] count = new int[26];
        for(int i=0;i<s.length();i++){
            count[s.charAt(i)-'a']++;
            count[t.charAt(i)-'a']--;
        }
        for(int i:count){
            if(i!=0){
                return false;
            }
        }
        return true;
    }
}
```

Do have a look at the discuss section for more optimized solutions if available - [LeetCode Discuss](https://leetcode.com/problems/valid-anagram/solutions/)