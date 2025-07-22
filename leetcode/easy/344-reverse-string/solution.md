# 344. Reverse String

**Link:** https://leetcode.com/problems/reverse-string/submissions/1707123315/

AmazonMicrosoftAdobeFacebooktcsWrite a function that reverses a string. The input string is given as an array of characters s. You must do this by modifying the input array in-place with O(1) extra memory.

```java
class Solution {
    public void reverseString(char[] s) {
        int st=0,e=s.length-1;
        while(st<e){
            char temp= s[st];
            s[st++]=s[e];
            s[e--]=temp;
        }
    }
}
```
