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
