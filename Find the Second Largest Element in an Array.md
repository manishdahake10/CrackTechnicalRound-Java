## Find the Second Largest Element in an Array (Java)

## **📜 Description**  
This Java program finds the second largest number in an array. It first sorts the array in ascending order and then returns the second last element as the second largest number.  

## **🚀 Features**  
- Simple and efficient approach  
- Uses built-in sorting for ease of implementation  
- Handles edge cases where the array has less than two elements  

## **💻 How It Works**  
1. The program checks if the array has at least two elements.  
2. It sorts the array in ascending order using `Arrays.sort()`.  
3. The second largest element is retrieved from the second last index.  
4. The result is printed to the console.  

## **📝 Code Example**  
```java
import java.util.Arrays;

public class SecondLargest {
    public static int findSecondLargest(int[] arr) {
        if (arr.length < 2) {
            throw new IllegalArgumentException("Array must have at least two elements.");
        }
        Arrays.sort(arr);
        return arr[arr.length - 2];
    }

    public static void main(String[] args) {
        int[] numbers = {10, 20, 5, 8, 30, 25};
        System.out.println("Second Largest Element: " + findSecondLargest(numbers));
    }
}
```

## **📌 Example Output**  
### **Input:**  
```java
int[] numbers = {10, 20, 5, 8, 30, 25};
```
### **Sorted Array:**  
```
[5, 8, 10, 20, 25, 30]
```
### **Output:**  
```
Second Largest Element: 25
```

## **📊 Complexity Analysis**  
- **Time Complexity:** \(O(n \log n)\) (Due to sorting)  
- **Space Complexity:** \(O(1)\) (No extra space used)  

## **⚠️ Edge Cases Considered**  
- Arrays with duplicate elements  
- Arrays with only two elements  
- Arrays with negative numbers  

## **📌 Alternative Approach (Without Sorting)**  
A more efficient solution exists using a single traversal (\(O(n)\)).
