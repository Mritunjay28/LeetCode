# All Divisors

**Link:** https://www.geeksforgeeks.org/batch/skill-up-dsa/track/su-dsa-topic-wise-week1/problem/all-divisors

Given a positive integer n, find all the distinct divisors of n.

```sort byaccuracy low to highaccuracy high to lowsubmmision low to highsubmmision high to lowdifficulty low to highdifficulty high to low
class Solution {
    public ArrayList<Integer> printDivisors(int n) {
    ArrayList<Integer>  arr = new ArrayList<>();
    for(int i=1;i<=Math.sqrt(n);i++){
        if(n%i==0){
            if(n/i==i) arr.add(i);
            else{
                arr.add(i);
                arr.add(n/i);
            }
        }
    }
    return arr;
    }
}
```
