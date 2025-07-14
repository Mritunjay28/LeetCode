# 76. Minimum Window Substring

**Link:** https://leetcode.com/problems/minimum-window-substring/description/

FacebookAmazonLinkedInLyftMicrosoftGiven two strings s and t of lengths m and n respectively, return the minimum window substring of s such that every character in t (including duplicates) is included in the window. If there is no such substring, return the empty string "". The testcases will be generated such that the answer is unique.

```java
class Solution {
    public String minWindow(String s, String t) {
        HashMap<Character , Integer> mapt = new HashMap<>();
        HashMap<Character , Integer> maps = new HashMap<>();
        for(char ch : t.toCharArray()){
            mapt.put(ch,mapt.getOrDefault(ch,0)+1);
        }

        int s=0,e=0,ans=0;
        while(e<s.length()){
            char ch= s.charAt(e);
            maps.put(ch,maps.getOrDefault(ch,0)+1); 

            




        }

    }
}
```
