# Lab 3: Asymptotic Analysis

This lab focuses on understanding and analyzing the asymptotic behavior of algorithms. We will explore concepts such as Big-O, Big-$\Theta$, and Big-$\Omega$ notations, and apply them to various algorithmic problems to determine their efficiency and scalability.

**Instructions:** To complete this lab, you may work in groups, but you must write your solutions yourself. Once you have completed the lab, push your changes to your forked repository.

## Problem 1

Suppose $T(n)$ is the worst case running time of an algorithm with input size $n$, and we know that $T(n)$ is $\mathcal{O}(n^3)$ and $\Omega(n^2)$. For each of the following statements, determine whether it must be true, must be false, or could be either true or false. Give a brief justification for each. 

1. $T(n)$ is $\mathcal{O}(n^2)$.
 - True; Since Big O is an upper bound, so since in this case T(n) is O(n^2) it falls under the worst case scenario of n^3
2. $T(n)$ is $\Theta(n^3)$.
 - True; Theta uses big O(upper bound) and big omega(lower bound) as a range of values that it can go through, since it is exactly n^3 which is the same as O(n^3) hence making it true.
3. $T(n)$ is $\Omega(n)$.
 - False; big omega is a lowerbound so for the value to be lower than the lowerbound would not be possible, making it false.
4. $T(n)$ is $\Theta(n^{1.5})$.
 - False; Theta cannot fall out of the range of big O and big Omega, in this statement it falls under big Omega so it has to be false.
5. $T(n)$ is $\mathcal{O}(n)$.
 - True; Since Big O is an upper bound, so since in this case T(n) is O(n) it falls under the worst case scenario of n^3
6. $T(n)$ is $\Theta(n^2 \log n)$.
 - Either, Because we know that initially it is going to be above the lowerbound of  however the log equation may increase it past the upperbound of O


## Problem 2
Consider the following algorithm where $f(A, i, j)$ is an unknown algorithm that takes as input an array $A$ and two indicies $i$ and $j$ and returns a number. 

```
Mystery Algorithm
Input: An array of int $A$ of length $n$.
Output: int sum
    n = |A|
    sum = 0
    for i = 1 to n:
        for j = 1 to n:
            sum += f(A, i, j)
```

Without knowing anything about $f$, what can we say about the running time of the Mystery Algorithm in terms of $n$? Justify your answer. 

Because we dont know anything about "f", the best we can do it assume based off of the rest of the code, which is O(n^2) plus any of the extra steps present. To find big O we drop any lower terms so in this case, our final time complexity  is O(n^2)