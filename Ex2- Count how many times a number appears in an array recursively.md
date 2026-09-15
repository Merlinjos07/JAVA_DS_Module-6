# Ex2 Count how many times a number appears in an array recursively.
## DATE:15.9.2026
## AIM:
To write a Java program to Count how many times a number appears in an array recursively.

## Algorithm
Start the program. Read the size of the array and input all elements into the array. Read the target number whose frequency you want to count. Call the recursive function countOccurrences(arr, index, target) If index == arr.length, return 0 If arr[index] == target, return 1 + countOccurrences(arr, index + 1, target) Else return countOccurrences(arr, index + 1, target) Display the returned count as the total number of occurrences.  

## Program:
```
/*
Program Count how many times a number appears in an array recursively.
Developed by: MERLIN M
RegisterNumber: 212225240084 
*/
import java.util.Scanner;

public class CountOccurrences {
    public static int countOccurrences(int[] arr, int n, int target) {
        if (n == 0) {
            return 0;
        }
        if (arr[n - 1] == target) {
            return 1 + countOccurrences(arr, n - 1, target);
        } else {
            return countOccurrences(arr, n - 1, target);
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int size = scanner.nextInt();

        if (size <= 0) {
            System.out.println("Invalid array size. Must be positive.");
            return;
        }

        int[] arr = new int[size];
        for (int i = 0; i < size; i++) {
            arr[i] = scanner.nextInt();
        }

        // Input: Target number to count
        int target = scanner.nextInt();

        int count = countOccurrences(arr, size, target);
        System.out.println("The number " + target + " appears " + count + " time(s) in the array.");

        scanner.close();
    }
}
```

## Output:

<img width="830" height="497" alt="image" src="https://github.com/user-attachments/assets/aee84b25-98bc-4323-bfb4-5ed714da1999" />


## Result:
Thus, the Java program to Count how many times a number appears in an array recursively is implemented successfully.
