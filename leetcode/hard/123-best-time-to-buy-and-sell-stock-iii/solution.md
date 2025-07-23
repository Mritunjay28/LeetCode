# 123. Best Time to Buy and Sell Stock III

**Link:** https://leetcode.com/problems/best-time-to-buy-and-sell-stock-iii/solutions/

AmazonUberAppleYou are given an array prices where prices[i] is the price of a given stock on the ith day. Find the maximum profit you can achieve. You may complete at most two transactions.

```java
    public int maxProfit(int[] prices) {
         int n = prices.length;
        if (n == 0) return 0;

        int[] leftProfit = new int[n]; // maxprofit if sell today or before today
        int[] rightProfit = new int[n]; // maxprofit if buy today or after today

        for(int i=1;i<n;i++){
            minprice=Math.min(minprice,prices[i]);
        } 
        int minprice=prices[0];
            leftProfit[i] = Math.max(leftProfit[i-1],prices[i]-minprice);

        int maxprice=prices[n-1];
        for(int i=n-2;i>=0;i--){
            maxprice=Math.max(maxprice,prices[i]);
            rightProfit[i] = Math.max(rightProfit[i+1],maxprice-prices[i]);
        } 

        int maxprofit=0;
        for(int i=0;i<n;i++){
            maxprofit=Math.max(maxprofit,leftProfit[i]+rightProfit[i]);
        }

        return maxprofit;

    }
```
