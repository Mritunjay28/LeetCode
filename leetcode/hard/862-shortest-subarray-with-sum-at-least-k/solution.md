# 862. Shortest Subarray with Sum at Least K

**Link:** https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/submissions/1709510036/

Given an integer array nums and an integer k, return the length of the shortest non-empty subarray of nums with a sum of at least k. If there is no such subarray, return -1. A subarray is a contiguous part of an array.

```java

        int ans = n + 1;
        Deque<Integer> dq = new LinkedList<>();

        for (int i = 0; i <= n; i++) {
            while (!dq.isEmpty() && prefix[i] - prefix[dq.peekFirst()] >= k) {
                ans = Math.min(ans, i - dq.pollFirst());
            }

            while (!dq.isEmpty() && prefix[i] < prefix[dq.peekLast()]) {
                dq.pollLast();
            }

            dq.offerLast(i);
        }

        for (int i = 0; i < n; i++) {
            prefix[i + 1] = prefix[i] + nums[i];
        }
        long[] prefix = new long[n + 1];  // Use long to prevent overflow

```
