# 53. Maximum Subarray

**Link:** https://leetcode.com/problems/maximum-subarray/description/

LinkedInAmazonAppleMicrosoftAdobeGiven an integer array nums, find the subarray with the largest sum, and return its sum.

```java
class Solution {
    public int maxSubArray(int[] nums) {
        int sum=0,max=Integer.MIN_VALUE;
        for(int i=0;i<nums.length;i++){
            if(sum<0) sum=0;

            sum+=nums[i];

            if(max<sum) max=sum;

        }
        return max;
    }
}
```
