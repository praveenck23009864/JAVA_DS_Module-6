# EX 1 You’re creating a health monitoring device which stores several sensor readings in an array. To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
## AIM:
To write a JAVA program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

## Algorithm
1. Start the program and read the number of sensor readings; store them in an array.

2. Define a recursive function findMin(arr, n) to find the minimum value among the first n elements.

3. Base Case: If only one element exists (n == 1), return that element.

4.  Recursive Case: Compare the last element with the minimum of the remaining elements and return the smaller value.

5.   Call the recursive function with the full array, display the minimum (lowest heartbeat), and stop the program.

## Program:
```
/*
Program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
Developed by: praveen ck
RegisterNumber: 212222243003
*/


import java.util.*;

public class MinimumValueRecursive {
    // Recursive method to find the minimum value in the array
    static int findMin(int[] arr, int n) {
        // Base case
        if (n == 1)
            return arr[0];
        // Recursive case
        return Math.min(arr[n - 1], findMin(arr, n - 1));
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of readings: ");
        int n = sc.nextInt();

        int[] readings = new int[n];
        System.out.println("Enter the readings:");
        for (int i = 0; i < n; i++) {
            readings[i] = sc.nextInt();
        }

        int minValue = findMin(readings, n);
        System.out.println("The minimum (lowest heartbeat) value is: " + minValue);
    }
}


```

## Output:

<img width="1919" height="560" alt="image" src="https://github.com/user-attachments/assets/2f4b9260-5be8-4db7-aa21-8715918cab23" />


## Result:
Thus the JAVA program to find the minimum value (e.g., lowest heartbeat), implement a recursive method has implemented successfully
