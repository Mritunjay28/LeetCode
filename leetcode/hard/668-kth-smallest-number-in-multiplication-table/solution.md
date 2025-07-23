# 668. Kth Smallest Number in Multiplication Table

**Link:** https://leetcode.com/problems/kth-smallest-number-in-multiplication-table/

RubrikNearly everyone has used the Multiplication Table. The multiplication table of size m x n is an integer matrix mat where mat[i][j] == i * j (1-indexed). Given three integers m, n, and k, return the kth smallest element in the m x n multiplication table.

```java
class Solution {
     public boolean enough(int x, int m, int n, int k) {
        int count = 0;
        for (int i = 1; i <= m; i++) {
    }

    public int findKthNumber(int m, int n, int k) {
        while (lo < hi) {
            int mi = lo + (hi - lo) / 2;
        int lo = 1, hi = m * n;
            if (!enough(mi, m, n, k)) lo = mi + 1;
            else hi = mi;
        }
        return count >= k;
            count += Math.min(x / i, n);
        }
        return lo;
    }
}
```
