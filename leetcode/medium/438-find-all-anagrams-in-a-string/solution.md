# 438. Find All Anagrams in a String

**Link:** https://leetcode.com/problems/find-all-anagrams-in-a-string/submissions/1695971955/

AmazonMicrosoftFacebookAppleAdobeGiven two strings s and p, return an array of all the start indices of p's anagrams in s. You may return the answer in any order.

```java
class Solution {
    public List<Integer> findAnagrams(String a, String p) {
        List<Integer> list = new ArrayList<>();
        Map<Character, Integer> map1 = new HashMap<>();
        Map<Character, Integer> map2 = new HashMap<>();
        for (char ch : p.toCharArray()) {
            map2.put(ch, map2.getOrDefault(ch, 0) + 1);
        }

        int s = 0, e = 0;

        while (e < a.length()) {
            map1.put(a.charAt(e), map1.getOrDefault(a.charAt(e), 0) + 1);

            if (e - s + 1 == p.length()) {
                if (map1.equals(map2)) {
                    list.add(s);
                }
                map1.put(a.charAt(s), map1.get(a.charAt(s)) - 1);
                if (map1.get(a.charAt(s)) == 0) {
                    map1.remove(a.charAt(s));
```
