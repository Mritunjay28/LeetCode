# Closest Number

**Link:** https://www.geeksforgeeks.org/batch/skill-up-dsa/track/su-dsa-topic-wise-week1/problem/closest-number5728

Given two integers n and m (m != 0). The problem is to find the number closest to n and divisible by m. If there is more than one such number, then output the one having the maximum absolute value.

```sort byaccuracy low to highaccuracy high to lowsubmmision low to highsubmmision high to lowdifficulty low to highdifficulty high to low
class Solution {
    static int closestNumber(int n, int m) {
        // code here
    double q= (double)n/m;
    double n1= m*Math.floor(q) ;
    double n2 = m*Math.ceil(q);
    double diff1 = Math.abs(n-n1);
    double diff2 = Math.abs(n-n2);
    if(diff1<diff2) return (int)n1 ;
    else if (diff2 < diff1) return (int)n2;
    else {
        if(Math.abs(n1)>Math.abs(n2)) return (int) n1;
        else return (int) n2 ;
    }
    }
}
```
