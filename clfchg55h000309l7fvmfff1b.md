---
title: "Reverse a Linked List"
seoTitle: "Coding Solution - Leetcode - Reverse a Linked List"
seoDescription: "Leetcode Solutions"
datePublished: Fri Mar 17 2023 11:54:41 GMT+0000 (Coordinated Universal Time)
cuid: clfchg55h000309l7fvmfff1b
slug: reverse-a-linked-list
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679053817061/496af840-bb69-40d9-a2bd-c6ef931c253c.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1679053981867/8ba3731b-1c59-4aae-8674-4d78d2043337.jpeg
tags: coding, leetcode, codenewbies, leetcode75, leetcode-solution

---

### Problem

Given the head of a singly linked list, reverse the list, and return *the reversed list*. This is similar to the Leetcode Problem - [Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/)

### Approach

The approach would be simple, create a null node, place it to the left of the first node and then reverse all the nodes from the right towards the null node.

```java
class Solution {
    public ListNode reverseList(ListNode head) {
        if(head ==null || head.next ==null)
            return head;
      ListNode newHead = null;
        while (head!=null) {
           ListNode next = head.next;
            head.next = newHead;
            newHead = head;
            head = next;
        }
        return newHead;
    }
}
```

Do have a look at the discuss section for more optimized solutions if available - [LeetCode Discuss](https://leetcode.com/problems/reverse-linked-list/discuss?currentPage=1&orderBy=most_votes&query=&tag=java)