# Decimal to binary

**Link:** https://www.geeksforgeeks.org/batch/skill-up-dsa/track/su-dsa-topic-wise-week1/problem/decimal-to-binary-1587115620

Given a decimal number n, return its binary equivalent.

```sort byaccuracy low to highaccuracy high to lowsubmmision low to highsubmmision high to lowdifficulty low to highdifficulty high to low
class Solution {
    static String decToBinary(int n) {
        // code here
        StringBuilder str = new StringBuilder();
        while(n>0){
            int rem= n%2;
            str.insert(0,rem);
            n/=2;
        }
        return str.toString();
    }
}
```
