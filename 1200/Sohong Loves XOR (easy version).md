## [Shohag Loves XOR (Easy Version)](https://codeforces.com/contest/2039/problem/C1)

#### My Aproach :

- Initially brute force.
- Then thaught of something like counting the number of setbits and unset bits and stuff.

#### Correct Approach :

- If P is divisible by a number X, then X has to be either P or X<=(P/2).
- So, if (x^y) divides X/Y , then it can at maximum be max(X/2 , Y/2).
- Now , how does x affect (x^y).
- For y to be divisible by (x^y) --> (x^y) must be <= Y/2.
- Take a look at MSB.
- Eg : Y --> 001xxxx , then some number that divided Y should have a MSB at a place atleast 1 lesser than Y.
- (Y/2) --> 0001xxx .
- So , if(y>x) then , more particularly , if y has s MSB greater the MSB of X , then the XOR val wil retain the Y's MSB.
- So , (X^Y) can't be divisor of x.
- _So , can it be divisor of Y?_
- Nope, since the Y and (X^Y) would be having the same MSB , but inorder to divide it should have MSB atleast 1 lesser than Y.
- But what if (X^Y) == Y , then the MSB is same and it also divides. But given that X>=1 and y>=1 , so that their (X^Y) != Y always holds.
- So the possible range of values if from 1 to 2X.

#### Solution

- [My Solution](https://codeforces.com/contest/2039/submission/340341751)
