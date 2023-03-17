---
title: "Linked List Cycle"
seoTitle: "Detect if the linked list has a cycle - leetcode"
datePublished: Fri Mar 17 2023 13:10:33 GMT+0000 (Coordinated Universal Time)
cuid: clfck5p0x000109mk506ja4my
slug: linked-list-cycle
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679058259147/326c7bf1-9234-4cf2-b21c-1e7baa47003b.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1679058583900/84ecb46d-76a2-414a-8f1e-dd02e48d4ed3.jpeg
tags: java, coding, leetcode, coding-challenge, linkedlists

---

### Problem

Given the head of a linked list, determine if the linked list has a cycle in it. This is similar to the Leetcode Problem - [Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/)

### Solution

The approach would be simple, take 2 pointers, slow as turtle and fast as hare. When the turtle is equal to the hare, cycle is found.

```java
public class Solution {
    public boolean hasCycle(ListNode head) {
        ListNode hare = head;
        ListNode turtle = head;
        while(hare!=null && hare.next !=null) {
        turtle = turtle.next ;
        hare = hare.next.next;
            if(hare == turtle)
                return true;
        }
        return false;    
    }
}
```

Do have a look at the discuss section for more optimized solutions if available - [LeetCode Discuss](https://leetcode.com/problems/linked-list-cycle/discuss/?currentPage=1&orderBy=most_votes&query=&tag=java)