# Java Programs: Palindrome Check

## 📌 Introduction

**Palindrome String Check**

## *📝 Palindrome String Check in Java*

*This program checks whether a given string is a ****palindrome**** (reads the same forward and backward).*

### *📍 Example:*

```
Input: "madam"
Output: "madam is a palindrome"

Input: "hello"
Output: "hello is not a palindrome"
```

### *🔹 Java Code:*

```java
public class PalindromeChecker {
    public static boolean isPalindrome(String str) {
        int left = 0, right = str.length() - 1;
        while (left < right) {
            if (str.charAt(left) != str.charAt(right)) {
                return false;
            }
            left++;
            right--;
        }
        return true;
    }

    public static void main(String[] args) {
        String input = "madam"; // Change this value to test different strings
        if (isPalindrome(input)) {
            System.out.println(input + " is a palindrome");
        } else {
            System.out.println(input + " is not a palindrome");
        }
    }
}
```

---

## 🔍 Explanation

### ✅ 1️⃣ Two-Pointer Approach

```java
int left = 0, right = str.length() - 1;
```

- Two pointers are used: `left` starts from the beginning, `right` starts from the end.

### ✅ 2️⃣ Character Comparison Loop

```java
while (left < right) {
    if (str.charAt(left) != str.charAt(right)) {
        return false;
    }
    left++;
    right--;
}
```

- If characters at `left` and `right` are not equal, return `false`.
- Move the pointers inward until they meet in the middle.

---

## ⏳ Time & Space Complexity

- **Time Complexity:** `O(n)`, as we check each character once.
- **Space Complexity:** `O(1)`, since no extra memory is used.

---

## 🔥 Summary
- **Palindrome Checker:** Uses a two-pointer approach for efficient palindrome detection.

---

