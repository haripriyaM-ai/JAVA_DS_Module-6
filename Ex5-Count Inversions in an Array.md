# Ex5 Count Inversions in an Array
## DATE:
## AIM:
To write a Java program  to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j

## Algorithm
1. Start
2. Read the number of elements n
3. Create an integer array arr of size n
4. Input all elements of the array
5. Initialize inversion count = 0
6. For each i from 0 to n-2
      For each j from i+1 to n-1
           If arr[i] > arr[j]
               Increment inversion count by 1
7. Display the total inversion count
8. Stop
 

## Program:
```java
/*
Program toto Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j
Developed by: HARI PRIYA M
RegisterNumber: 212224240047
*/

import java.util.Scanner;

public class CountInversions {

    public static int countInversions(int[] arr) {
        int count = 0;

        for (int i = 0; i < arr.length - 1; i++) {
            for (int j = i + 1; j < arr.length; j++) {
                if (arr[i] > arr[j]) {
                    count++;
                }
            }
        }

        return count;
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

        int inversions = countInversions(arr);
        System.out.println("Total number of inversions: " + inversions);

        sc.close();
    }
}

```

## Output:
<img width="407" height="263" alt="Screenshot 2025-11-23 142349" src="https://github.com/user-attachments/assets/9e225380-7847-40e9-ac4e-0ea92217d0b7" />



## Result:
Thus the Java program to to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < jis implemented successfully.
