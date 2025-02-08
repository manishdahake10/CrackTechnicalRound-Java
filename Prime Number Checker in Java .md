# Prime Number Checker in Java  

## Description  
This Java program checks whether a given number is prime or not.  
A **prime number** is a natural number greater than **1** that has only two factors: **1 and itself**.  

## How It Works  
- If the number is **less than or equal to 1**, it is **not prime**.  
- The program checks divisibility from **2 to the square root of the number**.  
- If the number is divisible by any value in this range, it is **not prime**.  
- Otherwise, it is a **prime number**.  

## Features  
✔ Checks if a number is prime  
✔ Uses an optimized **O(√N)** approach  
✔ Simple and efficient implementation  

## Code  
```java
public class PrimeChecker {
    public static void main(String[] args) {
        int number = 29; // Change this value to test other numbers
        boolean isPrime = isPrime(number);
        System.out.println(number + " is " + (isPrime ? "a Prime Number." : "not a Prime Number."));
    }

    public static boolean isPrime(int num) {
        if (num <= 1) return false; // Numbers <= 1 are not prime

        for (int i = 2; i <= Math.sqrt(num); i++) {
            if (num % i == 0) return false; // If divisible, it's not prime
        }
        return true; // If no divisors are found, it's prime
    }
}
```

## Output
```Result
29 is a Prime Number.

```
