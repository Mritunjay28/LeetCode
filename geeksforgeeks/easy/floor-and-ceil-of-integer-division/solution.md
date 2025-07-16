# Floor and Ceil of Integer Division

**Link:** https://www.geeksforgeeks.org/batch/skill-up-dsa/track/su-dsa-topic-wise-week1/problem/floor-and-ceil-of-integer-division

You are given two integers a and b (where b ≠ 0). The task is to compute both the floor division and ceiling division of the expression a / b. The floor of the division a / b , denoted as ⌊ a / b ⌋ is the greatest integer less than or equal to a / b. The ceil of the division a / b, denoted as  ⌈ a / b ⌉  is the smallest integer greater than or equal to a / b.

```sort byaccuracy low to highaccuracy high to lowsubmmision low to highsubmmision high to lowdifficulty low to highdifficulty high to low
class Solution {
    public ArrayList<Integer> divFloorCeil(int a, int b) {
        // code here
        ArrayList<Integer> arr = new ArrayList<>();
        arr.add((int)Math.floor((double)a/b));
        arr.add((int)Math.ceil((double)a/b));
        return arr;
    }
}
```
