# 81. Search in Rotated Sorted Array II

**Link:** https://leetcode.com/problems/search-in-rotated-sorted-array-ii/submissions/1452166365/

AmazonLinkedInAdobeFacebookThere is an integer array nums sorted in non-decreasing order (not necessarily with distinct values).

```java
        int s=0,e=nums.length-1;

        while(s<=e){
class Solution {
    public boolean search(int[] nums, int target) {
            int mid = s+(e-s)/2 ;
            if(nums[mid]==target) return true;
            if(nums[s]==nums[mid] && nums[e]==nums[mid]){
                s++;
                e--;
            }
            else if(nums[s]<=nums[mid]){
                if(nums[s]<=target && target<=nums[mid]) e=mid-1;
                else s=mid+1;
            }
            else {
                if(target<=nums[e] && nums[mid]<target) s=mid+1;
                else e=mid+1;
            }
        }

        return false;

```
