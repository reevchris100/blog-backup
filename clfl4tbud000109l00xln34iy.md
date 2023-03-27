---
title: "Maximum Depth of Binary Tree"
seoTitle: "Leetcode - Maximum depth of binary tree"
seoDescription: "Leetcode - Find the maximum depth of a binary tree given root of the tree."
datePublished: Thu Mar 23 2023 13:10:57 GMT+0000 (Coordinated Universal Time)
cuid: clfl4tbud000109l00xln34iy
slug: maximum-depth-of-binary-tree
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679576685260/9c6755e9-44d2-4835-9d40-9e62160144a8.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1679576988716/947ce600-422a-4cf1-a595-22e4b3ac90a7.jpeg
tags: tree, leetcode, maximum, depth

---

### Problem

Given the root of the binary tree, find its maximum depth. This is similar to the Leetcode Problem - [Maximum Depth of Binary Tree](https://leetcode.com/problems/maximum-depth-of-binary-tree/)

### Approach

The approach would be based on recursion where we traverse through the left and right nodes of the tree and find the maximum among them.

```java
class Solution {
    public int maxDepth(TreeNode root) {
int l = 0, r=0;
        if(root == null){
            return 0;
        }
        if(root.left != null){
            l = 1 + maxDepth(root.left);
        } 
        if(root.right != null){
            r = 1 + maxDepth(root.right);
        }
        if(root.left == null && root.right == null){
            return 1;
        }        
        return Math.max(l,r);
    }
}
```

Do have a look at the discuss section for more optimized solutions if available - [LeetCode Discuss](https://leetcode.com/problems/maximum-depth-of-binary-tree/solutions/)