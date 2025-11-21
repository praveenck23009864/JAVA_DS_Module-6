# Ex5 Count Inversions in an Array

## AIM:
To write a Java program  to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j

## Algorithm
1. Read the number of elements and store them in an array.

2. Define a recursive function that checks pairs of indices (i, j) such that i < j.

3. For each pair, check if arr[i] > arr[j]; if true, count it as an inversion.

4. Move through all pairs by increasing j, and when j ends, move to the next i.

5. Return and display the total number of inversions found.
 

## Program:
```
/*
Program toto Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j
Developed by: praveen ck
RegisterNumber: 212222243003
*/


import java.util.*;

public class InversionCountRecursive {

    // Recursive function to count inversions
    static int countInversions(int[] arr, int i, int j) {
        if (i >= arr.length - 1)
            return 0;
        if (j >= arr.length)
            return countInversions(arr, i + 1, i + 2);

        int count = (arr[i] > arr[j]) ? 1 : 0;
        return count + countInversions(arr, i, j + 1);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of elements: ");
        int n = sc.nextInt();

        int[] arr = new int[n];
        System.out.println("Enter array elements:");
        for (int i = 0; i < n; i++)
            arr[i] = sc.nextInt();

        int invCount = countInversions(arr, 0, 1);
        System.out.println("Number of inversions: " + invCount);
    }
}

```

## Output:

<img width="1919" height="618" alt="image" src="https://github.com/user-attachments/assets/78a5b072-4159-4425-b9b9-395135e97e4e" />


## Result:
Thus the Java program to to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < jis implemented successfully.
