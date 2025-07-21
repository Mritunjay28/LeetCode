# 3614. Process String with Special Operations II

**Link:** https://leetcode.com/problems/process-string-with-special-operations-ii/submissions/1695854186/

You are given a string s consisting of lowercase English letters and the special characters: '*', '#', and '%'. You are also given an integer k. Build a new string result by processing s according to the following rules from left to right: If the letter is a lowercase English letter append it to result. A '*' removes the last character from result, if it exists. A '#' duplicates the current result and appends it to itself. A '%' reverses the current result. Return the kth character of the final string result. If k is out of the bounds of result, return '.'.

