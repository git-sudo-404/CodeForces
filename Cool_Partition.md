## [Cool Partition](https://codeforces.com/problemset/problem/2117/C)

#### My Aproach

##### Observation :

- The elements with only one occurance and the last occurance of all the elements must belong to the last segment.
- Find the min index among the above elements and it marks the starting of last seg.
- Then the previous occurance of all the elements with the minimum index marks the starting of the last-1 segment.
- _Found it super hard to implement the above logic_

#### Correct Approach :

- _Key Insight : The nth segment should contain all the distinct elements from 1 till the ending of the nth segment_
- (i.e) Consider l and r to be the starting and ending of the nth segment then nth segment should contain all the distinct elements from 1 till r.

#### Solution

- [My Solution](https://codeforces.com/contest/2117/submission/337543272)
