# 76. Minimum Window Substring

**Link:** https://leetcode.com/problems/minimum-window-substring/

FacebookAmazonLinkedInLyftMicrosoftGiven two strings s and t of lengths m and n respectively, return the minimum window substring of s such that every character in t (including duplicates) is included in the window. If there is no such substring, return the empty string "". The testcases will be generated such that the answer is unique.

```java
        int st=0,e=0,ans=Integer.MAX_VALUE,counter=t.length();
        while(e<s.length()){
            arr[s.charAt(e)]--;
            if( arr[s.charAt(e)] >= 0) counter--;

            while(counter==0){
                if(ans>e-st+1){

           arr[ch]++;
        }
        for(char ch : t.toCharArray()){
                    ans=e-st+1;
        int minstart=0;
                    minstart=st;
                }
                arr[s.charAt(st)]++;
                if(arr[s.charAt(st)]==1) counter++;
                st++;
            }

            e++;
        }

        return (ans==Integer.MAX_VALUE)? "" : s.substring(minstart,minstart+ans);
        int[] arr = new int[128];
class Solution {
    public String minWindow(String s, String t) {
```
