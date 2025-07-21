# 2571. Minimum Operations to Reduce an Integer to 0

**Link:** https://leetcode.com/problems/minimum-operations-to-reduce-an-integer-to-0/

You are given a positive integer n, you can do the following operation any number of times: Add or subtract a power of 2 from n. Return the minimum number of operations to make n equal to 0. A number x is power of 2 if x == 2i where i >= 0.

```java
class·‌Solution·‌{
·‌·‌·‌·‌public·‌int·‌minOperations(int·‌n)·‌{
·‌·‌·‌·‌·‌·‌·‌·‌return·‌f(n);
·‌·‌·‌·‌}

·‌·‌·‌·‌public·‌int·‌f(int·‌n){
·‌·‌·‌·‌·‌·‌·‌·‌if(n==0){
·‌·‌·‌·‌·‌·‌·‌·‌·‌·‌·‌·‌return·‌0;
·‌·‌·‌·‌·‌·‌·‌·‌}

·‌·‌·‌·‌·‌·‌·‌·‌int·‌count1=0,count2=0;
·‌·‌·‌·‌·‌·‌·‌·‌int·‌near·‌=(int)·‌(Math.log(n)·‌/·‌Math.log(2))·‌;
·‌·‌·‌·‌·‌·‌·‌·‌int·‌a=(int)·‌Math.pow(2,near)·‌,·‌b=(int)Math.pow(2,near+1);·‌//·‌a=less·‌than·‌n,·‌b·‌is·‌
larger·‌than·‌n

·‌·‌·‌·‌·‌·‌·‌·‌if((n-a==0)·‌||(b-n==0)·‌)·‌return·‌1;
·‌·‌·‌·‌·‌·‌·‌·‌else{
·‌·‌·‌·‌·‌·‌·‌·‌·‌·‌·‌·‌//·‌Add·‌
·‌·‌·‌·‌·‌·‌·‌·‌·‌·‌·‌·‌count1+=·‌f(n-a);
·‌·‌·‌·‌·‌·‌·‌·‌·‌·‌·‌·‌count2+=f(b-n);
·‌·‌·‌·‌·‌·‌·‌·‌}
```
