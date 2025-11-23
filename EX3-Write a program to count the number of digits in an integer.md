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
