## [XOR & Triangle](https://codeforces.com/problemset/problem/2074/C)

#### My Aproach

- Thaught of setting the 1st set bit of x to y and taking xor to get z.
-       000001010100 --> x
-       000001000000 --> y
-       000000010100 --> z
- But found out this won't work on all testcases.

#### Correct Approach :

- expand the inequalities x + y > z , z + x > y , z + y > x , since z = x ^ y.
- using the formulae/ fact that x + y is the same as x ^ y + 2\*(x&y).
- ==> x + y > z
- ==> x + y > x ^ y
- ==> (x^y) + 2\*(x&y) > (x^y)
- ==> 2\*(x&y) > 0 (Subracted x^y from both sides)
- ==> x&y > 0 --> [1]

- ==> z + y > x
- ==> (x^y) + y > x
- ==> (x^y ^ y) + 2\*((x^y)&y) > x
- ==> x + 2\*((x^y)&y) > x
- ==> 2\* ((x^y) & y) > 0 (Subracted x from both sides)
- ==> (x^y) & y > 0 --> [2]

###### What does [1] and [2] Imply ?

##### [1] :

- x & y > 0 .
-       1010101 --> x
-       0101001   --> y
- x and y have atleast on bit in common.

##### [2] :

- (x^y) & y have atleast a bit in common.
- for a bit in y to stay set in x^y the bit in x should not be set.
-       000000000 --> x
-       000001000   --> y
-       000001000   --> x ^ y
- so a set bit y must be unset in x.

##### _Finally from [1] and [2]:_

- x and y must have a set bit in common.
- a set bit in y must be unset in x.

#### Solution

- [My Solution](https://codeforces.com/contest/2074/submission/337870560)
