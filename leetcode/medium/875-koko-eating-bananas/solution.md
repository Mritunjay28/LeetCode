# 875. Koko Eating Bananas

**Link:** https://leetcode.com/problems/koko-eating-bananas/submissions/1457762517/

Koko loves to eat bananas. There are n piles of bananas, the ith pile has piles[i] bananas. The guards have gone and will come back in h hours. Koko can decide her bananas-per-hour eating speed of k. Each hour, she chooses some pile of bananas and eats k bananas from that pile. If the pile has less than k bananas, she eats all of them instead and will not eat any more bananas during this hour. Koko likes to eat slowly but still wants to finish eating all the bananas before the guards return. Return the minimum integer k such that she can eat all the bananas within h hours.

```java
        while(s<e){
            int mid= s+(e-s)/2;

            if(possible(mid,piles,h)){
                e=mid;
            }
            else s=mid+1;
        }

        return s;
    }

    public boolean possible(int n,int[] piles, int h){
        int count=0;
        for(int banana:piles){
            if(banana<n) count++;
            else{
                int rem=(int)Math.ceil((double) banana/n);
                count+=rem;
            }
        }
     return count<=h;
    }
}
```
