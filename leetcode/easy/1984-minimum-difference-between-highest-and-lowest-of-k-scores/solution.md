# 1984. Minimum Difference Between Highest and Lowest of K Scores

**Link:** https://leetcode.com/problems/minimum-difference-between-highest-and-lowest-of-k-scores/submissions/1707986110/

You are given a 0-indexed integer array nums, where nums[i] represents the score of the ith student. You are also given an integer k. Pick the scores of any k students from the array so that the difference between the highest and the lowest of the k scores is minimized. Return the minimum possible difference.

```java
class Solution {
    public int minimumDifference(int[] nums, int k) {
       if(k==1) return 0;
       Arrays.sort(nums);
      int diff = Integer.MAX_VALUE; int i = 0 ;int j = i + k -1;
        while( j < nums.length){
                int temp = nums[j] - nums[i];
                j++;
                if(temp < diff) diff = temp;
                i++;
            }
        
        return diff;
    }
}
```
