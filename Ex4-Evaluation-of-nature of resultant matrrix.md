# Ex4 You are given a Java program that performs matrix addition. If Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension, what will be the nature (even/odd/mixed) of the resulting matrix?

## AIM:
To write a java function to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix.

## Algorithm

1. Read Matrix A where all elements are odd.

2. Read Matrix B where all elements are even and of the same dimension as A.

3. Add the corresponding elements: result[i][j] = A[i][j] + B[i][j].

4. Since odd + even always results in an odd number, every element in the resulting matrix will be odd.

5. Therefore, the resulting matrix is entirely odd.
  

## Program:
```
/*
Program to ind the nature of resultant matrrix.
Developed by: Ramya.P
RegisterNumber:  212223240137
*/


import java.util.*;

public class MatrixNature {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter rows: ");
        int r = sc.nextInt();
        System.out.print("Enter columns: ");
        int c = sc.nextInt();

        int[][] A = new int[r][c];
        int[][] B = new int[r][c];
        int[][] result = new int[r][c];

        System.out.println("Enter Matrix A (odd numbers):");
        for (int i = 0; i < r; i++)
            for (int j = 0; j < c; j++)
                A[i][j] = sc.nextInt();

        System.out.println("Enter Matrix B (even numbers):");
        for (int i = 0; i < r; i++)
            for (int j = 0; j < c; j++)
                B[i][j] = sc.nextInt();

        // Matrix addition
        for (int i = 0; i < r; i++)
            for (int j = 0; j < c; j++)
                result[i][j] = A[i][j] + B[i][j];

        System.out.println("Resulting Matrix:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++)
                System.out.print(result[i][j] + " ");
            System.out.println();
        }

        System.out.println("\nNature of Resulting Matrix: All values are ODD");
    }
}


```

## Output:

<img width="1919" height="622" alt="image" src="https://github.com/user-attachments/assets/559efc59-ede2-4485-be3c-cfdfdb8c63c5" />


## Result:
Thus, the java program to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix is implemented successfully.
