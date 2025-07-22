# 169. Majority Element

**Link:** https://leetcode.com/problems/majority-element/submissions/1707299822/

AmazonMicrosoftAdobeAppleGoogleGiven an array nums of size n, return the majority element. The majority element is the element that appears more than ⌊n / 2⌋ times. You may assume that the majority element always exists in the array.

```java
class Solution {
    public int majorityElement(int[] nums) {
        int currnum=nums[0] ,count=1;
        for(int i=1;i<nums.length;i++){
            if(nums[i]==currnum) count++;
            else count--;
            if(count==0) {
        }
        return currnum;

                currnum=nums[i];
            }
    }
                count++;
}
```
