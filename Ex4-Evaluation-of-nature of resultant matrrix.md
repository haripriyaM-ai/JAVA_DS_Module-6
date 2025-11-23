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
