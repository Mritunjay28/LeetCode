# 871. Minimum Number of Refueling Stops

**Link:** https://leetcode.com/problems/minimum-number-of-refueling-stops/submissions/1710750429/

A car travels from a starting position to a destination which is target miles east of the starting position. There are gas stations along the way. The gas stations are represented as an array stations where stations[i] = [positioni, fueli] indicates that the ith gas station is positioni miles east of the starting position and has fueli liters of gas. The car starts with an infinite tank of gas, which initially has startFuel liters of fuel in it. It uses one liter of gas per one mile that it drives. When the car reaches a gas station, it may stop and refuel, transferring all the gas from the station into the car. Return the minimum number of refueling stops the car must make in order to reach its destination. If it cannot reach the destination, return -1. Note that if the car reaches a gas station with 0 fuel left, the car can still refuel there. If the car reaches the destination with 0 fuel left, it is still considered to have arrived.

```java
    public int minRefuelStops(int target, int startFuel, int[][] stations) {
        if (startFuel >= target)
            return 0;
        if (stations.length == 0)
            return -1;
        int count = 0, distance = 0, current = startFuel;
        PriorityQueue<Integer> pq = new PriorityQueue<>((a, b) -> b - a);

        for (int i = 0; i < stations.length; i++) {

            if (current < stations[i][0] - distance) {
                if (pq.isEmpty() && distance < target)
                    return -1;
                else {
                    while (!pq.isEmpty() && current < stations[i][0] - distance) {
                        current += pq.poll();
                        count++;
                    }
                    if (current < stations[i][0] - distance)
                        return -1;
                }
            }

            current = current - (stations[i][0] - distance);
            distance = distance + (stations[i][0] - distance);

            pq.offer(stations[i][1]);
```
