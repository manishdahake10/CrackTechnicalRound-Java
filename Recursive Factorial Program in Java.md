# Recursive Factorial Program in Java

## 📌 Introduction
This Java program calculates the factorial of a number using **recursion**. The factorial of a number `n` (denoted as `n!`) is the product of all natural numbers from `1` to `n`.

### 📍 Example:
```
5! = 5 × 4 × 3 × 2 × 1 = 120
```

---

## 📝 Java Program
```java
public class Factorial {
    // Recursive function to calculate factorial
    public static int factorial(int n) {
        // Base case: if n is 0 or 1, return 1
        if (n == 0 || n == 1) {
            return 1;
        }
        // Recursive case: n * factorial(n - 1)
        return n * factorial(n - 1);
    }

    public static void main(String[] args) {
        int num = 5; // Change this value to test different numbers
        System.out.println("Factorial of " + num + " is: " + factorial(num));
    }
}
```

---

## 🔍 Explanation
### ✅ 1️⃣ Base Case (Stopping Condition)
```java
if (n == 0 || n == 1) {
    return 1;
}
```
- If `n == 0` or `n == 1`, return `1`. This prevents infinite recursion.

### ✅ 2️⃣ Recursive Case (Function Calls Itself)
```java
return n * factorial(n - 1);
```
- Calls the function with `n - 1`, reducing problem size until the base case is reached.

---

## 🔢 Step-by-Step Execution
For **n = 5**, the recursive calls work as follows:

| Function Call | Returns | Calculation |
|--------------|---------|-------------|
| `factorial(5)` | `5 * factorial(4)` | `5 × 24 = 120` |
| `factorial(4)` | `4 * factorial(3)` | `4 × 6 = 24` |
| `factorial(3)` | `3 * factorial(2)` | `3 × 2 = 6` |
| `factorial(2)` | `2 * factorial(1)` | `2 × 1 = 2` |
| `factorial(1)` | `1` (Base case) | |

Final result: **`120`** (for `5!`).

---

## ⏳ Time & Space Complexity
- **Time Complexity:** `O(n)`, as we make `n` recursive calls.
- **Space Complexity:** `O(n)`, due to the function call stack.

---

## ⚠️ Limitations & Alternative Approach
- **Limitation:** If `n` is very large (e.g., `n > 1000`), it may cause a **stack overflow** error.
- **Solution:** Use an **iterative approach** or **tail recursion** for better efficiency.

---

## 🔥 Summary
- Recursion provides a simple way to calculate factorial.
- Base case ensures termination (`n == 0` or `n == 1`).
- Each recursive call reduces the problem size.
- The function keeps calling itself until it reaches the base case.

---

