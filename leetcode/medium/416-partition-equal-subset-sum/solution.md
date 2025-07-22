# 416. Partition Equal Subset Sum

**Link:** https://leetcode.com/problems/partition-equal-subset-sum/submissions/1653272695/

FacebookMicrosoftAmazonAppleGoogleGiven an integer array nums, return true if you can partition the array into two subsets such that the sum of the elements in both subsets is equal or false otherwise.

```java

        if(currentsum==target){
            return backtrack(nums,used,k-1,0,0,target);
        }

        for(int i=start;i<nums.length;i++){
            if(used[i] || nums[i]+currentsum>target) continue;

            used[i]=true;
            if (backtrack(nums,used,k,i+1,currentsum+nums[i],target)) return true;
            used[i]=false;

            if(currentsum==0) break;
        }

        return false;
    }
}
```
