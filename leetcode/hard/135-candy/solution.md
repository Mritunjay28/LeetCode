# 135. Candy

**Link:** https://leetcode.com/problems/candy/submissions/1698374107/

AmazonThere are n children standing in a line. Each child is assigned a rating value given in the integer array ratings. You are giving candies to these children subjected to the following requirements: Each child must have at least one candy. Children with a higher rating get more candies than their neighbors. Return the minimum number of candies you need to have to distribute the candies to the children.

```java
class Solution {
    public int candy(int[] ratings) {
        int[] candy = new int[n];

        for(int i=0;i<n;i++){
            if(i>0 && ratings[i]>ratings[i-1]){
                candy[i]=candy[i-1]+1;
            }
        }

        for(int i=n-1;i>=0;i--){
        int n=ratings.length;
        Arrays.fill(candy,1);
            if(i<n-1 && ratings[i]>ratings[i+1]){
                if(candy[i+1]+1>candy[i]) candy[i]=candy[i+1]+1;
            }
        }

        int ans=0;
        for(int a :candy) ans+=a;

        return ans;
    }
} 
```
