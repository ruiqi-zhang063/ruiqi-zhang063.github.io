Title: Homework 1  
Date: 09/03/2021   
Author: Ruiqi Zhang  
Slug: Homework 1
Category: Homework 1

# Homework 1 - Math Fun

#### Problem 123 - Prime square remainders (solved by 11386 people, I am the 11387th.)

Let $p_n$ be the $n$th prime: $2, 3, 5, 7, 11, ...,$ and let $r$ be the remainder when $(p_n−1)^n + (p_n+1)^n$ is divided by $p_n^2$.

For example, when $n = 3$, $p_3 = 5$, and $4^3 + 6^3 = 280 ≡ 5$ mod $25$.

The least value of $n$ for which the remainder first exceeds $10^9$ is $7037$.

Find the least value of $n$ for which the remainder first exceeds $10^{10}$.

#### Solution 

In this question, we can first generate a prime list. For any new number, if it cannot be divisible by any prime number smaller than it, then it is also a prime number. 

Then when we get a new prime, and the index in prime list plus 1 is the n. Then every time we obtain a new prime number, we can use the formula from question to test whether it is the number we want. If it meet the requirement, we can change the value of parameter 'requirement' to stop the while loop.

The answer is 21035.

#### Problem 125 - Palindromic sums (solved by 13356 people, I am the 13357th.)

The palindromic number 595 is interesting because it can be written as the sum of consecutive squares:  $6^2 + 7^2 + 8^2 + 9^2 + 10^2 + 11^2 + 12^2$.

There are exactly eleven palindromes below one-thousand that can be written as consecutive square sums, and the sum of these palindromes is $4164$. Note that $1 = 0^2 + 1^2$ has not been included as this problem is concerned with the squares of positive integers.

Find the sum of all the numbers less than $10^8$ that are both palindromic and can be written as the sum of consecutive squares.

#### Solution

The largest consecutive number is less than or equal to int(sqrt(number/2))+1 because we need at least two square number. The formula for sum for consecutive squares from 1 to n is n(n+1)(2n+1)/6.
Then the formula for sum for consecutive squares from $n_1$ to $n_2$ is $n_2(n_2+1)(2n_2+1)/6-n_1(n_1+1)(2n_1+1)/6$.

From the subtraction of two non-adjacent numbers in the sum_square_array, we can find all numbers that can be written as the sum of consecutive squares and then test whether they are palindormic.

Some of the number maybe repeated. We can use sum(set()) to remove repeating.

The answer is 2906969179.

#### Proble 347 - Largest integer divisible by two primes (solved by 4402, I am the 4403th.)

The largest integer ≤ 100 that is only divisible by both the primes 2 and 3 is 96, as $96=32*3=2^5*3$. For two distinct primes p and q let M(p,q,N) be the largest positive integer ≤N only divisible by both p and q and M(p,q,N)=0 if such a positive integer does not exist.

E.g. M(2,3,100)=96.
M(3,5,100)=75 and not 90 because 90 is divisible by 2 ,3 and 5.
Also M(2,73,100)=0 because there does not exist a positive integer ≤ 100 that is divisible by both 2 and 73.

Let S(N) be the sum of all distinct M(p,q,N). S(100)=2262.

Find S(10 000 000).

#### Solution

In this question, we can also first generate a prime list. For any new number, if it cannot be divisible by any prime number smaller than it, then it is also a prime number. In fact, we only need to test the prime number smaller sqrt of this new number.

Then for any two different primes p and q, if their product is smaller than required N, then M(p,q,N) will be larger than 0. Suppose q is the larger prime, and $q^{n_2}<N, q^{n_2+1}>N$, then we decrease $n_2$ in turn, and find $n_1$ that is not 0 and make $q^{n_2}p^{n_1}<N, q^{n_2}p^{n_1+1}>N$. In this processing, temp will be replaced by the largest  $q^{n_2}p^{n_1}$. Then the final temp will be the M(p,q,N). Sum all the M(p,q,N) and we get the result.

The answer is 11109800204052.
