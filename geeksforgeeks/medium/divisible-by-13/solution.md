# Divisible by 13

**Link:** https://www.geeksforgeeks.org/batch/skill-up-dsa/track/su-dsa-topic-wise-week1/problem/divisible-by-13

Given a number represented as a string s (which may be very large), check whether it is divisible by 13 or not.

```sort byaccuracy low to highaccuracy high to lowsubmmision low to highsubmmision high to lowdifficulty low to highdifficulty high to low
class Solution {
    public boolean divby13(String s) {
        // code here
        int mod =0;
        for(int i=0;i<s.length();i++){
            char ch = s.charAt(i);
            int digit = ch-'0';
            mod= (mod *10+ digit) %13;
        }
         return mod==0;
    }
}
```
