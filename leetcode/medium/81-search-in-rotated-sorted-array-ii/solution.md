# 81. Search in Rotated Sorted Array II

**Link:** https://leetcode.com/problems/search-in-rotated-sorted-array-ii/submissions/1452166365/

AmazonLinkedInAdobeFacebookThere is an integer array nums sorted in non-decreasing order (not necessarily with distinct values).

```java
        int s=0,e=nums.length-1;

        while(s<=e){
            int mid = s+(e-s)/2 ;
        }
            if(nums[mid]==target) return true;
            else if (nums[s]>=nums[mid] ) e=mid-1;
            else s=mid+1;

        return false;
class Solution {
    public boolean search(int[] nums, int target) {

    }
}
```
