# [2523. Closest Prime Numbers in Range](https://leetcode.com/problems/closest-prime-numbers-in-range/description/)

## Key Takeways

- Learn **Sieve of Eratosthenes** algorithm to find all prime numbers up to a given limit, n
- **Algorithm**

    1. **Input:** A number `n` (the upper limit for prime numbers).
    2. **Create a list** `isPrime` of size `n+1` initialized to `true`. This list will help track whether each number is prime or not. Set `isPrime[0] = false` and `isPrime[1] = false` since 0 and 1 are not primes.

    3. **Iterate** over numbers `i` from 2 to √n.
        - If `isPrime[i]` is `true`, then:
            - Mark all multiples of `i` starting from `i * i` as `false` (since they are not primes, we start marking its multiples from `i * i` instead of `2 * i`. This is because smaller multiples of `i` (like `2 * i`, `3 * i`, etc.) would have already been marked by smaller primes.).
    
    4. The **remaining numbers** that are still marked `true` in the `isPrime` list are prime numbers.
