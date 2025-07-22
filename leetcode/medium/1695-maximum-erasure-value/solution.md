# 1695. Maximum Erasure Value

**Link:** https://leetcode.com/problems/maximum-erasure-value/submissions/1706917440/

CashfreeYou are given an array of positive integers nums and want to erase a subarray containing unique elements. The score you get by erasing the subarray is equal to the sum of its elements. Return the maximum score you can get by erasing exactly one subarray. An array b is called to be a subarray of a if it forms a contiguous subsequence of a, that is, if it is equal to a[l],a[l+1],...,a[r] for some (l,r).

```java
class Solution {
    public int maximumUniqueSubarray(int[] nums) {
        int max=0;
        int[] arr = new int[10001];
        int s=0,e=0,sum=0;
        while(e<nums.length){
            arr[nums[e]]++;

            while(arr[nums[e]]>1){
                max=Math.max(max,sum);
                arr[nums[s]]--;
                sum-=nums[s];
                s++;
            }
            sum+=nums[e];
            e++;
        }
```
