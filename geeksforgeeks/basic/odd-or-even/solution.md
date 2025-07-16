# Odd or Even

**Link:** https://www.geeksforgeeks.org/batch/skill-up-dsa/track/su-dsa-topic-wise-week1/problem/odd-or-even3618

Given a positive integer n, determine whether it is odd or even. Return true if the number is even and false if the number is odd.

```sort byaccuracy low to highaccuracy high to lowsubmmision low to highsubmmision high to lowdifficulty low to highdifficulty high to low
class Solution {
    static boolean isEven(int n) {
        // code here
        if((n & 1)==0) return true ;
        return false;
    }
}
```
