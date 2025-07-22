# 45. Jump Game II

**Link:** https://leetcode.com/problems/jump-game-ii/description/

AmazonAppleBloombergGoogleDoorDashYou are given a 0-indexed array of integers nums of length n. You are initially positioned at nums[0]. Each element nums[i] represents the maximum length of a forward jump from index i. In other words, if you are at nums[i], you can jump to any nums[i + j] where: 0 <= j <= nums[i] and i + j < n Return the minimum number of jumps to reach nums[n - 1]. The test cases are generated such that you can reach nums[n - 1].

```java
class Solution {
    public int jump(int[] nums) {
        int near=0,far=0,jump=0; // near=start , far=end till we can go at that particular instance
        while(far<nums.length-1){ // stop when can go more than n-1 elemnt or equal
            int farthest =0; // record farthest we can go now
            for(int i=near;i<=far;i++){ // travel for all values accessable noe
                farthest=Math.max(farthest,i+nums[i]); 
            }
            near=far+1;
            far=farthest;
            jump++;
        }

        return jump;
    }
}
```
