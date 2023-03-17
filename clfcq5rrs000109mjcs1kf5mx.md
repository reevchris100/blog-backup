---
title: "Longest Common Subsequence"
seoTitle: "Longest Common Subsequence of two strings"
seoDescription: "Leetcode - Longest Common Subsequence of two strings"
datePublished: Fri Mar 17 2023 15:58:34 GMT+0000 (Coordinated Universal Time)
cuid: clfcq5rrs000109mjcs1kf5mx
slug: longest-common-subsequence
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679058189405/93d7ea3f-e30f-439e-8606-5164ea325a40.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1679068666837/2d94ae8c-56ed-4a46-9ae8-5ad16da4c255.jpeg
tags: algorithms, data-structures, coding, leetcode, codebuzz

---

### Problem

Given two strings text1 and text2, return the length of their longest common subsequence. If there is no common subsequence, return 0. This is similar to the Leetcode Problem - [Longest Common Subsequence](https://leetcode.com/problems/longest-common-subsequence/)

### Approach

The approach would be based on dynamic programming. We take a 2d array with rows and columns indicating string 1 and string 2 respectively. Then we use the below code to calculate the common subsequence of the previous diagonal element if equal else we take the max of the upper and left element.

```java
class Solution {
    public int longestCommonSubsequence(String text1, String text2) {
int m = text1.length(), n = text2.length();
        int[][] dp = new int[m + 1][n + 1];
        for(int i = 1; i <= m; i++)
            for(int j = 1; j <= n; j++)
                if(text1.charAt(i-1) == text2.charAt(j-1)) dp[i][j] = dp[i-1][j-1] + 1;
                else dp[i][j] = Math.max(dp[i - 1][j], dp[i][j - 1]);
        return dp[m][n];
    }
}
```

Do have a look at the discuss section for more optimized solutions if available - [LeetCode Discuss](https://leetcode.com/problems/longest-common-subsequence/discuss/?currentPage=1&orderBy=most_votes&query=&tag=java)