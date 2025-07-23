# 480. Sliding Window Median

**Link:** https://leetcode.com/problems/sliding-window-median/submissions/1708023715/

FacebookSpotifyMicrosoftHBOThe median is the middle value in an ordered integer list. If the size of the list is even, there is no middle value. So the median is the mean of the two middle values.

```java
    public double[] medianSlidingWindow(int[] nums, int k) {
        double[] ans = new double[nums.length - k + 1];
        for (int i = 0; i < k; i++) {
            addNum(nums[i]);
        }
        ans[0] = getMedian();

        for (int i = k; i < nums.length; i++) {
            addNum(nums[i]);
            removeNum(nums[i - k]);
            ans[i - k + 1] = getMedian();
        }
    }

    // Main function that slides the window across the array
        } else {
            return right.peek() * 1.0;
        }
```
