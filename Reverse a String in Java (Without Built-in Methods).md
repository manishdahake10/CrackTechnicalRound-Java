# Reverse a String in Java (Without Built-in Methods)

## Description
This Java program reverses a given string without using built-in methods like `StringBuilder.reverse()`.  
It demonstrates basic string manipulation using loops.

## How It Works
- Iterates through the string in reverse order.
- Appends each character to a new string.
- Prints the reversed string.

## Code
```java
public class ReverseString {
    public static void main(String[] args) {
        String str = "Hello";
        String reversed = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            reversed += str.charAt(i);
        }

        System.out.println("Reversed String: " + reversed);
    }
}
```
## Output

```result
Reversed String: olleH
```
