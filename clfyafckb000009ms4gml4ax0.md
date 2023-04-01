---
title: "Happy Number"
seoTitle: "Leetcode Solution - Happy Number"
seoDescription: "Leetcode solution to find the happy number - Coding Solution"
datePublished: Sat Apr 01 2023 18:09:03 GMT+0000 (Coordinated Universal Time)
cuid: clfyafckb000009ms4gml4ax0
slug: happy-number
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1680371332392/774e6e0e-1eee-4395-9e7f-a48d05587743.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1680372453926/314a2c05-3244-4868-b11f-439278a72493.jpeg
tags: coding, leetcode, solutions, leetcode-solution, happynumber

---

### Problem

Write an algorithm to determine if a number is happy. A happy number is a number where the sum of the squares of each of its digits is found repeatedly till the result is 1. This is similar to the Leetcode Problem - [Happy Number](https://leetcode.com/problems/happy-number/)

### Approach

The approach would be defining a hash set which would store the summation of each of the digits. It would return false if the hash set already contains the result. This will be in loop till the result equals to 1 and then we return true.

```java
class Solution {
    public boolean isHappy(int n) {
        HashSet<Integer> set = new HashSet<Integer>();
        set.add(n);
        while (n != 1) {
            int result = 0;
            while (n != 0) {
                result += Math.pow(n % 10, 2);
                n /= 10;
            }
            if (set.contains(result)) {
                return false;
            }
            set.add(result);
            n = result;
        }
        return true;
    }
}
```

Do have a look at the discuss section for more optimized solutions if available - [LeetCode Discuss](https://leetcode.com/problems/happy-number/solutions/)