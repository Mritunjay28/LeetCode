# 1109. Corporate Flight Bookings

**Link:** https://leetcode.com/problems/corporate-flight-bookings/submissions/1711750330/

There are n flights that are labeled from 1 to n. You are given an array of flight bookings bookings, where bookings[i] = [firsti, lasti, seatsi] represents a booking for flights firsti through lasti (inclusive) with seatsi seats reserved for each flight in the range. Return an array answer of length n, where answer[i] is the total number of seats reserved for flight i.

```java
class Solution {
    public int[] corpFlightBookings(int[][] bookings, int n) {
        int[] ans = new int[n];

        for(int[] p : bookings){
           ans[p[0]-1] +=p[2]; // to the start add seats
        }

        return ans;
    }

           if(p[1] < n) ans[p[1]] -=p[2]; // to the end +1 subtract seats

        for(int i=1;i<n;i++) ans[i]+=ans[i-1]; // add all previous seats 
           // for last we have add at n position which will give out of index so skip it;
}
```
