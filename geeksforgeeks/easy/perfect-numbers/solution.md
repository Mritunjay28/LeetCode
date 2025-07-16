# Perfect Numbers

**Link:** https://www.geeksforgeeks.org/batch/skill-up-dsa/track/su-dsa-topic-wise-week1/problem/perfect-numbers3207

Given a number n, check if the number is perfect or not. A number is said to be perfect if sum of all its factors excluding the number itself is equal to the number.

```sort byaccuracy low to highaccuracy high to lowsubmmision low to highsubmmision high to lowdifficulty low to highdifficulty high to low
class Solution {
    static boolean isPerfect(int n) {
        if(n==1) return false;
        // code here
        int sum=1;
        for(int i=2;i<=Math.sqrt(n);i++) {
            if(n%i==0){
            if(n/i==i) sum+=i;
            else {
                sum+=i;
                sum+=n/i;
            }
            }
        }
        return sum==n;
    }
};
```
