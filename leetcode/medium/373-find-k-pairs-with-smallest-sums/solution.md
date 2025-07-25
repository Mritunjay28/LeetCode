# 373. Find K Pairs with Smallest Sums

**Link:** https://leetcode.com/problems/find-k-pairs-with-smallest-sums/

You are given two integer arrays nums1 and nums2 sorted in non-decreasing order and an integer k. Define a pair (u, v) which consists of one element from the first array and one element from the second array. Return the k pairs (u1, v1), (u2, v2), ..., (uk, vk) with the smallest sums.

```java
        while(k>0 && !pq.isEmpty()){
            int[] pair = pq.poll();

        for(int n:nums1) pq.offer(new int[]{n+nums2[0], 0});

        PriorityQueue<int []> pq = new PriorityQueue<>((a,b)-> a[0]-b[0]); 
        //a[0] =sum, a[1]= position in nums2
            int sum= pair[0];
            int posof2 = pair[1];

            // add to answer
            ans.add(List.of(sum-nums2[posof2], nums2[posof2]));

            if(posof2+1<nums2.length){
                pq.offer(new int[]{sum-nums2[posof2]+nums2[posof2 + 1], posof2+1});
            }

            k--;
        }

        return ans;
                
```
