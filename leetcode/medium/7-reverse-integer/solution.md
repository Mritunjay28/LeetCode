# 7. Reverse Integer

**Link:** https://leetcode.com/problems/reverse-integer/submissions/1510281859/

AdobeAmazonGoogleAppleFacebookGiven a signed 32-bit integer x, return x with its digits reversed. If reversing x causes the value to go outside the signed 32-bit integer range [-231, 231 - 1], then return 0. Assume the environment does not allow you to store 64-bit integers (signed or unsigned).

```java
class Solution {
    public int reverse(int x) {
        int sign=1;
        if(x<0) {
         sign=-1;
         x*=-1;
        }

         int ans=0;
        while(x>0){
            ans=ans*10+x%10;
            x/=10;
        }

        ans*=sign;

        return ans;

    }
}
```
