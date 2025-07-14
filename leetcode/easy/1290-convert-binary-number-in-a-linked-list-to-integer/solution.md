# 1290. Convert Binary Number in a Linked List to Integer

**Link:** https://leetcode.com/problems/convert-binary-number-in-a-linked-list-to-integer/submissions/1697091285/

AmazonOracleGiven head which is a reference node to a singly-linked list. The value of each node in the linked list is either 0 or 1. The linked list holds the binary representation of a number. Return the decimal value of the number in the linked list. The most significant bit is at the head of the linked list.

```java
 *     ListNode() {}
 *     ListNode(int val) { this.val = val; }
 *     ListNode(int val, ListNode next) { this.val = val; this.next = next; }
 * }
 */
class Solution {
 *     ListNode next;
    public int getDecimalValue(ListNode head) {
     int i=0;
       while(head!=null){
        i=i*2+head.val;
        head=head.next;
       } 
      
       return i;
    }
}
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
```
