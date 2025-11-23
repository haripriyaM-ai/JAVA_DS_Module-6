# Ex2 Count how many times a number appears in an array recursively.
## DATE:
## AIM:
To write a Java program to Count how many times a number appears in an array recursively.

## Algorithm
1. Start
2. Read number of elements n
3. Create an integer array arr of size n
4. Read the array elements
5. Read the target element to count
6. Call the recursive function countOccurrences(arr, 0, target)
7. In countOccurrences:
      - If index == array length, return 0
      -  If arr[index] == target, set count = 1, else count = 0
      -   Return count + countOccurrences(arr, index + 1, target)
8. Print the returned result as total occurrences
9. Stop

## Program:
```java
/*
Program Count how many times a number appears in an array recursively.
Developed by: HARI PRIYA M
RegisterNumber: 212224240047
*/

import java.util.Scanner;

public class RecursiveCount {
    
    public static int countOccurrences(int[] arr, int index, int target) {
        if (index == arr.length) {   // Base case: end of array
            return 0;
        }

        int count = (arr[index] == target) ? 1 : 0;
        return count + countOccurrences(arr, index + 1, target); // Recursive addition
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of elements: ");
        int n = sc.nextInt();

        int[] arr = new int[n];
        System.out.println("Enter the array elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        System.out.print("Enter the number to search: ");
        int target = sc.nextInt();

        int occurrences = countOccurrences(arr, 0, target);
        System.out.println(target + " appears " + occurrences + " time(s) in the array.");

        sc.close();
    }
}

```

## Output:
<img width="419" height="265" alt="image" src="https://github.com/user-attachments/assets/4fe62044-1c1b-4a90-b4ec-7543a5a115c8" />



## Result:
Thus, the Java program to Count how many times a number appears in an array recursively is implemented successfully.
