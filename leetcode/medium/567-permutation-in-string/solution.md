# 567. Permutation in String

**Link:** https://leetcode.com/problems/permutation-in-string/submissions/1692734661/

MicrosoftAppleYandexOracleAmazonGiven two strings s1 and s2, return true if s2 contains a permutation of s1, or false otherwise. In other words, return true if one of s1's permutations is the substring of s2.

```java
        HashMap<Character,Integer> s2Count = new HashMap<>();

        for(int i=0;i<s1.length();i++){
            s1Count.put(s1.charAt(i),s1Count.getOrDefault(s1.charAt(i),0)+1);
            s2Count.put(s2.charAt(i),s2Count.getOrDefault(s2.charAt(i),0)+1);
        }

        if(s1Count.equals(s2Count)) return true;

        int left=0,right=s1.length();
        while(right<s2.length()){
            char RightChar = s2.charAt(right);
            s2Count.put(RightChar,s2Count.getOrDefault(RightChar,0)+1);

            char LeftChar = s2.charAt(left);
            s2Count.put(LeftChar,s2Count.get(LeftChar)-1);

```
