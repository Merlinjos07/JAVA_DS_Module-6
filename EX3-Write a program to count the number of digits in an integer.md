# EX3 Write a program to count the number of digits in an integer.
## DATE:15.9.2026
## AIM:
To write a C program to implement Tower of Hanoi

## Algorithm
Read the input number Take an integer num from the user. Convert the number to a non-negative value Use Math.abs(num) and store it in n to handle negative numbers. Check if the number is zero If n == 0, set digit count to 1 (since zero has one digit). Count digits for non-zero numbers Repeatedly divide n by 10 and increment the counter until n becomes 0. Display the digit count Output the total number of digits. 

## Program:
```
/*
Program to to count the number of digits in an integer
Developed by: MERLIN M
RegisterNumber:212225240084
*/
import java.util.Scanner;

public class CountDigits {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();

        int count = 0;
        int n = Math.abs(num); 

        if (n == 0) {
            count = 1; 
        } else {
            while (n > 0) {
                n /= 10; 
                count++;
            }
        }

        System.out.println("Number of digits: " + count);
    }
}
```

## Output:

<img width="822" height="353" alt="image" src="https://github.com/user-attachments/assets/caf5a18a-63ac-4e1a-93a0-90193e260c86" />


## Result:
Thus, the Java program to to count the number of digits in an integer is implemented successfully.
