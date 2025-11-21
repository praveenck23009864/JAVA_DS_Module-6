# EX3 Write a program to count the number of digits in an integer.
## DATE:
## AIM:
To write a C program to implement Tower of Hanoi

## Algorithm
1. Start the program and read the integer input.

2. Define a recursive function countDigits(n) that returns the number of digits.

3. If n becomes 0, return 0 (base condition).

4. Otherwise return 1 + countDigits(n / 10) to count each digit.

5. Call the recursive function and display the total digit count.  

## Program:
```
/*
Program to to count the number of digits in an integer
Developed by: praveen ck
RegisterNumber:  212222243003
*/


import java.util.*;

public class CountDigitsRecursive {

    // Recursive function to count digits
    static int countDigits(int n) {
        if (n == 0)
            return 0;
        return 1 + countDigits(n / 10);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter an integer: ");
        int num = sc.nextInt();

        // Handle case where input is 0
        if (num == 0) {
            System.out.println("Number of digits: 1");
        } else {
            num = Math.abs(num); // handle negative numbers
            int digits = countDigits(num);
            System.out.println("Number of digits: " + digits);
        }
    }
}


```

## Output:

<img width="1919" height="616" alt="image" src="https://github.com/user-attachments/assets/f495f6fa-a165-4372-aa2d-45aefbd2db60" />


## Result:
Thus, the Java program to to count the number of digits in an integer is implemented successfully.
