# 347. Top K Frequent Elements

**Link:** https://leetcode.com/problems/top-k-frequent-elements/submissions/1709827912/

FacebookAmazonMicrosoftGoogleOracleGiven an integer array nums and an integer k, return the k most frequent elements. You may return the answer in any order.

```java
      }
        if(pq.size()>k) pq.poll();

     int[] ans = new int[k];
      for(int i=k-1;i>=0;i--){
        ans[i]=pq.poll()[0];

      for(Map.Entry<Integer,Integer> enter : map.entrySet()){
        pq.offer(new int[]{enter.getKey(), enter.getValue()});

      PriorityQueue<int[]> pq = new PriorityQueue<>((a,b)-> Integer.compare(a[1],b[1]));
      }
```
