### Fibonacci Series (Recursive & Iterative)

## **📌 Overview**  
This project demonstrates the Fibonacci series generation using **two methods** in Java:  
1. **Recursive Approach**  
2. **Iterative Approach**  

The Fibonacci series is a sequence where each number is the sum of the two preceding ones, starting from **0 and 1**.  

**Example Output:**  
`0, 1, 1, 2, 3, 5, 8, 13, 21, 34, ...`  

---

## **🔹 Fibonacci Series Implementation**  

### **1️⃣ Recursive Approach**  
**📌 Code:**
```java
public class FibonacciRecursive {
    public static int fibonacci(int n) {
        if (n <= 1) return n;
        return fibonacci(n - 1) + fibonacci(n - 2);
    }

    public static void main(String[] args) {
        int n = 10; 
        System.out.print("Fibonacci Series (Recursive): ");
        for (int i = 0; i < n; i++) {
            System.out.print(fibonacci(i) + " ");
        }
    }
}
```

#### 📌 Explanation:  
✔ Uses **recursion** to compute Fibonacci numbers.  
✔ **Base case:** If `n` is 0 or 1, return `n`.  
✔ **Recursive case:** Return `fibonacci(n-1) + fibonacci(n-2)`.  

⚡ **Time Complexity:** `O(2^n)` (Exponential, slow)  
⚡ **Space Complexity:** `O(n)` (Due to recursive stack calls)  

---

### **2️⃣ Iterative Approach**  
**📌 Code:**
```java
public class FibonacciIterative {
    public static void main(String[] args) {
        int n = 10; 
        int first = 0, second = 1;

        System.out.print("Fibonacci Series (Iterative): " + first + " " + second + " ");

        for (int i = 2; i < n; i++) {
            int next = first + second;
            System.out.print(next + " ");
            first = second;
            second = next;
        }
    }
}
```

**📌 Explanation:**  
✔ Uses a **loop** to compute Fibonacci numbers.  
✔ Initializes `first = 0` and `second = 1`.  
✔ Iterates `n-2` times, updating values accordingly.  

⚡ **Time Complexity:** `O(n)` (Linear, fast)  
⚡ **Space Complexity:** `O(1)` (Constant, efficient)  

---

## **⚖ Comparison Table**
| Method      | Approach | Time Complexity | Space Complexity | Efficiency |
|------------|---------|----------------|-----------------|------------|
| **Recursive** | Uses function calls | `O(2^n)` | `O(n)` | ❌ Slow for large `n` |
| **Iterative** | Uses a loop | `O(n)` | `O(1)` | ✅ Faster & recommended |

---

## **📢 Conclusion**  
🔹 **Recursive method** is simple but inefficient for large values of `n`.  
🔹 **Iterative method** is faster and more memory-efficient.  
🔹 **For large inputs, always prefer the iterative approach.**  

---
