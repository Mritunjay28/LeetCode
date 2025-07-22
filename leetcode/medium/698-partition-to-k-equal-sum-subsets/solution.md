# 698. Partition to K Equal Sum Subsets

**Link:** https://leetcode.com/problems/partition-to-k-equal-sum-subsets/submissions/1702377939/

LinkedInGoogleAmazonGiven an integer array nums and an integer k, return true if it is possible to divide this array into k non-empty subsets whose sums are all equal.

```java

        if(sum%k!=0) return false;

        int target= sum/k;

        if(max>target) return false;
        Arrays.sort(nums);
        return f(nums,k,target,0,0);
    }

    public boolean f(int[] nums, int k, int target , int currentsum , int start){
        if(k==1) return true;

        if(currentsum==target) return f(nums,k-1,target,0,start);

        for(int i =start ;i<nums.length;i++){
            if(nums[i]+currentsum >target) break;

            f(nums,k,target,currentsum+nums[i],i+1);
        }

        return false;

    }
}
```
