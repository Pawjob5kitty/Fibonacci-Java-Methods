---------------------------------------------------------------------------

1️⃣ Iterative Version
---------------------
Code:
public static long fibIterative(int n) {
    long prev = 0;
    long current = 1;
    
    for (int i = 0; i < n; i++) {
        long next = prev + current;
        prev = current;
        current = next;
    }
    
    return prev; // F(n)
}

Explanation:
- This is the simplest iterative approach to calculate Fibonacci numbers.
- Uses a loop to build the sequence step by step.
- Time complexity: O(n)
- Space complexity: O(1)
- Pros: Simple, fast for small and medium n, no recursion overhead.
- Cons: Not suitable for extremely large numbers due to `long` overflow.

---------------------------------------------------------------------------

2️⃣ Two-Step Iteration
---------------------
Code:
public static long fibTwoStep(int n) {
    long f1 = 0;
    long f2 = 1;

    for (int i = 0; i < n / 2; i++) {
        long temp1 = f1 + f2;
        long temp2 = f2 + temp1;
        f1 = temp1;
        f2 = temp2;
    }

    if (n % 2 == 0) return f1;
    else return f2;
}

Explanation:
- Optimized version that computes two Fibonacci numbers per loop iteration.
- Reduces the number of iterations roughly by half.
- Time complexity: O(n/2) → effectively O(n)
- Space complexity: O(1)
- Pros: Faster than simple iteration for large n.
- Cons: Slightly more complex logic; still limited by `long` overflow.

---------------------------------------------------------------------------

3️⃣ Recursive + Memoization
--------------------------
Code:
public static long fibMemo(int n, long[] memo) {
    if (n <= 1) return n;
    if (memo[n] != 0) return memo[n];
    
    memo[n] = fibMemo(n - 1, memo) + fibMemo(n - 2, memo);
    return memo[n];
}

Explanation:
- Classic recursive Fibonacci with memoization (caching) to avoid repeated calculations.
- Time complexity: O(n)
- Space complexity: O(n) (for memo array + recursion stack)
- Pros: Efficient recursion, easy to understand the logic.
- Cons: Uses extra memory; recursion depth may be a problem for very large n.

---------------------------------------------------------------------------

4️⃣ Fast Doubling (Recursive)
----------------------------
Code:
public static long[] fibFastDoubling(long n) {
    if (n == 0) return new long[]{0, 1};

    long[] half = fibFastDoubling(n / 2);
    long f_k = half[0];
    long f_k_plus_1 = half[1];

    long f_2k = f_k * (2 * f_k_plus_1 - f_k);
    long f_2k_plus_1 = f_k * f_k + f_k_plus_1 * f_k_plus_1;

    if (n % 2 == 0) return new long[]{f_2k, f_2k_plus_1};
    else return new long[]{f_2k_plus_1, f_2k + f_2k_plus_1};
}

Explanation:
- Fast doubling formula: computes Fibonacci numbers using divide and conquer.
- Time complexity: O(log n)
- Space complexity: O(log n) due to recursion stack
- Pros: Very fast, suitable for extremely large n if using BigInteger.
- Cons: More complex; requires understanding of doubling formula.

---------------------------------------------------------------------------

5️⃣ Binet Formula (Approximation)
--------------------------------
Code:
public static long fibBinet(int n) {
    double phi = (1 + Math.sqrt(5)) / 2;
    return Math.round(Math.pow(phi, n) / Math.sqrt(5));
}

Explanation:
- Uses closed-form Binet formula: F(n) = φ^n / √5
- Time complexity: O(1)
- Space complexity: O(1)
- Pros: Extremely fast, no loops or recursion.
- Cons: Only approximate; can be inaccurate for large n due to floating-point precision.

---------------------------------------------------------------------------

6️⃣ BigInteger Version (Safe for Large n)
-----------------------------------------
Code:
import java.math.BigInteger;

public static BigInteger fibBig(int n) {
    BigInteger prev = BigInteger.ZERO;
    BigInteger current = BigInteger.ONE;

    for (int i = 0; i < n; i++) {
        BigInteger next = prev.add(current);
        prev = current;
        current = next;
    }

    return prev;
}

Explanation:
- Iterative version using BigInteger to handle very large Fibonacci numbers.
- Time complexity: O(n)
- Space complexity: O(1)
- Pros: Can calculate Fibonacci numbers far beyond `long` limit.
- Cons: Slower than primitive long arithmetic; BigInteger operations are more expensive.

---------------------------------------------------------------------------
