# 1094. Car Pooling

**Link:** https://leetcode.com/problems/car-pooling/submissions/1711735333/

AmazonDoorDashFlipkartGoogleMicrosoftThere is a car with capacity empty seats. The vehicle only drives east (i.e., it cannot turn around and drive west). You are given the integer capacity and an array trips where trips[i] = [numPassengersi, fromi, toi] indicates that the ith trip has numPassengersi passengers and the locations to pick them up and drop them off are fromi and toi respectively. The locations are given as the number of kilometers due east from the car's initial location. Return true if it is possible to pick up and drop off all passengers for all the given trips, or false otherwise.

```java
class Solution {
    public boolean carPooling(int[][] trips, int capacity) {
       int[] stop = new int[1001]; // total distance which can be given 1 to 1000

       for(int[] t : trips){
        stop[t[1]] += t[0];  // At starting point add passanger

        stop[t[2]] -= t[0];  // At end point subtract passanger
       } 

       for(int i=0 ; capacity>=0 && i<stop.length;i++ ) capacity-=stop[i];
// when we pick passanger we subtract them from capacity , when leave we add to capacity

        return capacity>=0;
    }
}
```
