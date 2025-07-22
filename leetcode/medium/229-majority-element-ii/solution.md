# 229. Majority Element II

**Link:** https://leetcode.com/problems/majority-element-ii/submissions/1707307303/

AmazonMicrosoftAdobeGiven an integer array of size n, find all elements that appear more than ⌊ n/3 ⌋ times.

```java
class Solution {
    public List<Integer> majorityElement(int[] nums) {
        List<Integer> arr = new ArrayList<>();
        HashMap<Integer,Integer> map = new HashMap<>();

        for(int n : nums) map.put(n,map.getOrDefault(n,0)+1);

        for(int n : map.keySet()){

        int floor = (int)Math.floor((double)nums.length/3);
            if(map.get(n)>floor) arr.add(n);
        }

```
