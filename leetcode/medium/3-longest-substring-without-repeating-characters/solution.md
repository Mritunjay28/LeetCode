# 3. Longest Substring Without Repeating Characters

**Link:** https://leetcode.com/problems/longest-substring-without-repeating-characters/description/

AmazonMicrosoftFacebookBloombergAppleGiven a string s, find the length of the longest substring without duplicate characters.

```java
class Solution {
    public int lengthOfLongestSubstring(String s) {
        int[] charIndex = new int[128]; 
        for (int i = 0; i < 128; i++) charIndex[i] = -1; 

        int left = 0, maxLength = 0;

        for (int right = 0, n = s.length(); right < n; right++) {
            char c = s.charAt(right); 
            if (charIndex[c] != -1) {
                left = Math.max(left, charIndex[c] + 1); 
            }
            charIndex[c] = right;
            maxLength = Math.max(maxLength, right - left + 1);
        }

        return maxLength;


    }


    
}
```
