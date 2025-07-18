# 473. Matchsticks to Square

**Link:** https://leetcode.com/problems/matchsticks-to-square/description/

MicrosoftYou are given an integer array matchsticks where matchsticks[i] is the length of the ith matchstick. You want to use all the matchsticks to make one square. You should not break any stick, but you can link them up, and each matchstick must be used exactly one time. Return true if you can make this square and false otherwise.

```java
class Solution {
    public boolean makesquare(int[] nums) {
      int sum=0;
        for( int n:nums) sum+=n;
        if(sum%4!=0) return false;

        int target=sum/4;
        
        Arrays.sort(nums);
        int n=nums.length;

        boolean[] used = new boolean[n];

        return backtrack(nums,used,4,0,0,target);
    }

     public boolean backtrack(int[] nums,boolean[] used , int k , int start, int currentsum,
int target){
        if(k==1) return true; // if k-1 have equal value then automatically remain sum is 
equal to target as sum%k

        if(currentsum==target){
            return backtrack(nums,used,k-1,0,0,target);
        }

        for(int i=start;i<nums.length;i++){
```
