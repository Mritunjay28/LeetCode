# 435. Non-overlapping Intervals

**Link:** https://leetcode.com/problems/non-overlapping-intervals/submissions/1702295729/

Given an array of intervals intervals where intervals[i] = [starti, endi], return the minimum number of intervals you need to remove to make the rest of the intervals non-overlapping.

```java
class Solution {
    public int eraseOverlapIntervals(int[][] intervals) {
        if(intervals.length==1)return 0;
        Arrays.sort(intervals, (a,b)-> Integer.compare(a[1],b[1]));
        int count=0,i=0;

        for(int j=1;j<intervals.length;j++){
            if(intervals[i][1]<=intervals[j][0]){
                i=j;
            }
            else{
                count++;
            }
        }

        return count;

    }
}
```
