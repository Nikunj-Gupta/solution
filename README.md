## Question
Finding number of strings without contiguous 0s.
	
## Answer
The solution can be done iteratively or recursively. We can maintain two arrays, one beginning with 0 and the other beginning with 1. We can append 0 or 1 at the end of the second array but can append only 1 at the end of the first kind of array. This can go upto a length of n.
But this is an expensive solution. And for the given constraints we have to find something better.
On looking at the pattern of the answers, we can say that the answer to length N is (N-2)th fibonacci number.
So, finding (N-2)th fibonacci number mod 10^9+7 for a simpler answer.
This is fast.
But for constraints like N = 10^15, we need to be faster than that. For that we can store the recursive values in a map which can be used again and again while recursion.
Final solution is below. It is written in C++. Compile along with use of -std=c++11.


### Usage

Compile using ```g++ soln.cpp -std=c++11```
Run using ```./a.out```.
Or, use ```make``` to run the makefile.
