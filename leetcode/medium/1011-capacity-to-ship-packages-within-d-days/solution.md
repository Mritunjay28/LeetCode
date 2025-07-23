# 1011. Capacity To Ship Packages Within D Days

**Link:** https://leetcode.com/problems/capacity-to-ship-packages-within-d-days/submissions/1708386566/

A conveyor belt has packages that must be shipped from one port to another within days days. The ith package on the conveyor belt has a weight of weights[i]. Each day, we load the ship with packages on the conveyor belt (in the order given by weights). We may not load more weight than the maximum weight capacity of the ship. Return the least weight capacity of the ship that will result in all the packages on the conveyor belt being shipped within days days.

```java
                ans=mid;
                e=mid;
            }
            else s=mid+1;
        }

        return (ans==0)?sum:ans;
    }

    public boolean feasible(int n,int target,int[] weights){
            int mid= s+(e-s)/2;

            if(feasible(mid,days,weights)){

        int s=max,e=sum,ans=0;
        while(s<e){
            max=Math.max(max,n);
        }
        int sum=0,max=0;
        for(int n:weights) {
            sum+=n;
class Solution {
    public int shipWithinDays(int[] weights, int days) {
```
