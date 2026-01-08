
# Fibonacci Methods in Java

This repository contains different implementations of the Fibonacci sequence in Java. Each method demonstrates a unique approach with different performance characteristics.

## Methods

1️⃣ **Iterative Version**  
Simple iterative calculation of Fibonacci numbers.

2️⃣ **Two-Step Iteration**  
Optimized iterative version that computes two Fibonacci numbers per loop iteration.

3️⃣ **Recursive + Memoization**  
Classic recursive approach with memoization to avoid redundant calculations.

4️⃣ **Fast Doubling (Recursive)**  
Efficient recursive method using the fast doubling formula, suitable for large numbers.

5️⃣ **Binet Formula (Approximation)**  
Calculates Fibonacci using the closed-form formula. Note: approximation errors may occur for large n.

6️⃣ **BigInteger Version**  
Safe for very large n using `BigInteger` to avoid integer overflow.

## Usage

1. Clone the repository.
2. Copy the desired method into your Java project.
3. Call the function with the required parameter `n` to get the Fibonacci number.

```java
long result = fibIterative(50);
