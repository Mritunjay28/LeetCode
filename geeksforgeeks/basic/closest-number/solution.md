# Closest Number

**Link:** https://www.geeksforgeeks.org/batch/skill-up-dsa/track/su-dsa-topic-wise-week1/problem/closest-number5728

Given two integers n and m (m != 0). The problem is to find the number closest to n and divisible by m. If there is more than one such number, then output the one having the maximum absolute value.

```sort byaccuracy low to highaccuracy high to lowsubmmision low to highsubmmision high to lowdifficulty low to highdifficulty high to low
class Solution {
    static int closestNumber(int n, int m) {
        // code here
        int rem=n%m;
        int max=-100001 ;
        if((n+rem)%m==0)  max=Math.max(max,n+rem);
        if((n-rem)%m==0) {
            if(max==-100001) max=Math.max(max,n-rem);
            else {
                if(Math.abs(n+rem)> Math.abs(n-rem)) max= n+rem ;
                else max=n-rem;
            }
        }
       return max;
    }
}
```
