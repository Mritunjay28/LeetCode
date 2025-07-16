# 3201. Find the Maximum Length of Valid Subsequence I

**Link:** https://leetcode.com/problems/find-the-maximum-length-of-valid-subsequence-i/editorial/

You are given an integer array nums. A subsequence sub of nums with length x is called valid if it satisfies: (sub[0] + sub[1]) % 2 == (sub[1] + sub[2]) % 2 == ... == (sub[x - 2] + sub[x - 1]) % 2. Return the length of the longest valid subsequence of nums. A subsequence is an array that can be derived from another array by deleting some or no elements without changing the order of the remaining elements.

```java
class Solution {
    public int maximumLength(int[] nums) {
        // same parity  [1,1,1,1] [2,2,2]
       int even=0,odd=0;
       for(int n: nums) {
           if(n%2==0) even++ ;
           else odd++;
       }
        int maxlength = Math.max(even,odd);

        // Alternate parity [1,2,1,2,1]
        int endeven=0,endodd=0;
        for(int n:nums){
            if(n%2==0) {
                endeven = endodd +1 ;
            }
            else endodd= endeven +1 ; 
        }
         int maxAlternatelength = Math.max(endeven,endodd);
        
        return Math.max(maxlength , maxAlternatelength);
    }
}
```
