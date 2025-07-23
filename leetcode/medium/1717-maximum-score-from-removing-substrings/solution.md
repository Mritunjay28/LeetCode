# 1717. Maximum Score From Removing Substrings

**Link:** https://leetcode.com/problems/maximum-score-from-removing-substrings/submissions/1707942648/

GoogleYou are given a string s and two integers x and y. You can perform two types of operations any number of times. Remove substring "ab" and gain x points.

```java
                    ans+=x;
        // check for ab;
        for(char ch : s.toCharArray()){
            if(!stack.isEmpty() && ch=='b' && stack.peek()=='a'){
       }
       else{
         Stack<Character> stack = new Stack<>();
        }


                    stack2.pop();
            }
            else stack2.push(curr);
            if(!stack2.isEmpty() && curr=='a' && stack2.peek()=='b'){
                    ans+=x;
        Stack<Character> stack2 = new Stack<>();
        while(!stack.isEmpty()){
            char curr= stack.pop();
                    ans+=y;
                    stack.pop();
            }
            else stack.push(ch);
        }
        // check for ab
        for(char ch : s.toCharArray()){
            if(!stack.isEmpty() && ch=='a' && stack.peek()=='b'){
```
