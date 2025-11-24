# EX 1 You’re creating a health monitoring device which stores several sensor readings in an array. To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
## DATE:

## AIM:
To write a JAVA program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

## Algorithm
1. Start
2. Read the number of sensor readings n
3. Create an integer array arr of size n
4. Input all array elements (sensor values)
5. Call the recursive function findMin(arr, 0)
6. In findMin:
      a. If index == last index, return arr[index]
      b. Otherwise, find minimum of remaining values using findMin(arr, index + 1)
      c. Compare arr[index] with the returned minimum value
      d. Return the smaller value
7. Receive the result and print the minimum value
8. Stop
 

## Program:
```java
/*
Program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
Developed by: HARI PRIYA M 
RegisterNumber: 212224240047
*/

import java.util.Scanner;

public class RecursiveMin {
    
    public static int findMin(int[] arr, int index) {
        if (index == arr.length - 1) {   // Base case
            return arr[index];
        }

        int minRest = findMin(arr, index + 1); // Recursive call
        return Math.min(arr[index], minRest);  // Compare and return smaller
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of sensor readings: ");
        int n = sc.nextInt();

        int[] arr = new int[n];
        System.out.println("Enter the readings:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        int minimum = findMin(arr, 0);
        System.out.println("Lowest reading recorded: " + minimum);

        sc.close();
    }
}

```

## Output:
<img width="438" height="248" alt="image" src="https://github.com/user-attachments/assets/22e5def5-8c0a-40e3-9ea0-bb2cc16dd245" />



## Result:
Thus the JAVA prograM ti find the minimum value (e.g., lowest heartbeat), implement a recursive method has implemented successfully

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

# EX3 Write a program to count the number of digits in an integer.
## DATE:
## AIM:
To Write a program to count the number of digits in an integer using recursion.

## Algorithm
1. Start
2. Read an integer number num
3. If num is 0, print 1 and stop
4. Convert num to absolute value (handle negative numbers)
5. Call the recursive function countDigits(num)
6. In countDigits:
      - If num equals 0, return 0
      -  Else return 1 + countDigits(num / 10)
7. Print the returned result as the number of digits
8. Stop


## Program:
```java
/*
Program to to count the number of digits in an integer
Developed by: HARI PRIYA M
RegisterNumber: 212224240047
*/

import java.util.Scanner;

public class CountDigitsRecursive {

    public static int countDigits(int num) {
        if (num == 0) {   // Base case
            return 0;
        }
        return 1 + countDigits(num / 10);   // Recursive call
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int num = sc.nextInt();

        if (num == 0) {
            System.out.println("Number of digits: 1");
        } else {
            int count = countDigits(Math.abs(num)); // handle negative numbers
            System.out.println("Number of digits: " + count);
        }

        sc.close();
    }
}
```

## Output:
<img width="390" height="200" alt="image" src="https://github.com/user-attachments/assets/887d1487-4a50-48a1-b39e-b1e1374e6f39" />



## Result:
Thus, the Java program to to count the number of digits in an integer is implemented successfully.

# Ex4 You are given a Java program that performs matrix addition. If Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension, what will be the nature (even/odd/mixed) of the resulting matrix?
## DATE:
## AIM:
To write a java function to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix.

## Algorithm
1. Start
2. Read the number of rows and columns
3. Create three matrices A, B, and C of size rows × cols
4. Input elements of Matrix A (all odd numbers)
5. Input elements of Matrix B (all even numbers)
6. Initialize nature = "odd"
7. Perform matrix addition:
      For each i from 0 to rows-1
         For each j from 0 to cols-1
             C[i][j] = A[i][j] + B[i][j]
8. Display the resultant matrix C
9. Display the nature of the resultant matrix as "odd"
10. Stop


## Program:
```java
/*
Program to ind the nature of resultant matrrix.
Developed by: HARI PRIYA M
RegisterNumber: 212224240047
*/

import java.util.Scanner;

public class MatrixAdditionCheck {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the number of rows: ");
        int rows = sc.nextInt();
        System.out.print("Enter the number of columns: ");
        int cols = sc.nextInt();

        int[][] A = new int[rows][cols];
        int[][] B = new int[rows][cols];
        int[][] C = new int[rows][cols];

        System.out.println("Enter matrix A (odd numbers only):");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                A[i][j] = sc.nextInt();
            }
        }

        System.out.println("Enter matrix B (even numbers only):");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                B[i][j] = sc.nextInt();
            }
        }

        String nature = "odd";  

        System.out.println("Resultant Matrix C (A + B):");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                C[i][j] = A[i][j] + B[i][j];
                System.out.print(C[i][j] + " ");
            }
            System.out.println();
        }

        System.out.println("\nNature of the Result Matrix: " + nature);

        sc.close();
    }
}
```

## Output:
<img width="467" height="493" alt="image" src="https://github.com/user-attachments/assets/92b97b53-f3be-4da6-af33-69ef5c3623ee" />



## Result:
Thus, the java program to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix is implemented successfully.

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
