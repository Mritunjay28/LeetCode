# 209. Minimum Size Subarray Sum

**Link:** https://leetcode.com/problems/minimum-size-subarray-sum/submissions/1707995705/

FacebookAmazonMicrosoftBloombergGoldman SachsGiven an array of positive integers nums and a positive integer target, return the minimal length of a subarray whose sum is greater than or equal to target. If there is no such subarray, return 0 instead.

```java
class Solution {
    public int minSubArrayLen(int target, int[] nums) {
        int s=0,e=0,sum=0,minlength=1000000;
        while(e<nums.length){
            sum+=nums[e];

            while(sum>=target){
                minlength=Math.min(minlength,e-s+1);
                sum-=nums[s++];
            }

            e++;
        }

        return (minlength==1000000) ? 0 : minlength;
    }
}
```
