# 179. Largest Number

**Link:** https://leetcode.com/problems/largest-number/submissions/1698408903/

SalesforceMicrosoftFacebookAmazonAppleGiven a list of non-negative integers nums, arrange them such that they form the largest number and return it. Since the result may be very large, so you need to return a string instead of an integer.

```java
       
        String[] numstring = new String[nums.length];
        for (int i = 0; i < nums.length; i++) {
            numstring[i] = Integer.toString(nums[i]); 
        }

    
        Arrays.sort(numstring, (a, b) -> (b + a).compareTo(a + b));

       
        if (numstring[0].equals("0")) { // if largest num 0 then return 0
            return "0";
        }

       
        StringBuilder sb = new StringBuilder();
        for (String numStr : numstring) {
            sb.append(numStr);
        }

        return sb.toString();
    public String largestNumber(int[] nums) {
class Solution {
        // if(a,b) let be (2,3)  if (32).compare(23) if 32 > 26 then order (3,2) else (2,3)
       // covert to string as want to compare concation 
```
