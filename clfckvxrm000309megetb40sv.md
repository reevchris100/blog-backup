---
title: "Linked List Cycle - Get Node at Intersection"
seoTitle: "Get the node intersecting the linked list cycle"
seoDescription: "Leetcode - Get the node intersecting the linked list cycle"
datePublished: Fri Mar 17 2023 13:30:57 GMT+0000 (Coordinated Universal Time)
cuid: clfckvxrm000309megetb40sv
slug: linked-list-cycle-get-node-at-intersection
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679059451900/fa827f06-dc04-437f-957c-9329a8522837.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1679059805748/99fba9b2-b183-48ad-9b70-b9ef679a7368.jpeg
tags: hackathon, java, community, coding, leetcode

---

### Problem

Given the head of a linked list, return the node where the cycle begins. If there is no cycle, return null. This is similar to the Leetcode Problem - [Linked List Cycle II](https://leetcode.com/problems/linked-list-cycle-ii/)

### Approach

The approach would be similar to a linked list cycle, take 2 pointers, slow as turtle and fast as hare. When turtle is equal to hare, the cycle is found. Once the cycle is found, slow will start from head. Both slow and fast will traverse and when they are equal again, that node is the start of the cycle.

```java
public class Solution {
    public ListNode detectCycle(ListNode head) {
        ListNode slow = head, fast = head;
        
        while(fast!=null && fast.next !=null) {
            slow = slow.next;
            fast = fast.next.next;
            
            if(slow == fast) {
                slow = head;
                
                while (slow!=fast) {
                    slow = slow.next;
                    fast = fast.next;
                }
                return slow;
            }
        }
        return null;
    }
}
```

Do have a look at the discuss section for more optimized solutions if available - [Linked List Cycle II](https://leetcode.com/problems/linked-list-cycle-ii/discuss/?currentPage=1&orderBy=most_votes&query=&tag=java)