# EX 1 You’re creating a health monitoring device which stores several sensor readings in an array. To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
## DATE:15.9.2026
## AIM:
To write a JAVA program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

## Algorithm
Read the number of elements n and input all n integers into an array arr. Start the recursive function getMin(arr, 0, n) to find the minimum element. Inside the recursive function, check if the current index i is the last index (i == n−1).If yes, return arr[i] as the minimum. Otherwise, recursively call getMin(arr, i+1, n) to find the minimum of the remaining elements. Compare the current element arr[i] with the minimum of the rest and return the smaller value.   

## Program:
```
/*
Program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
Developed by: MERLIN M
RegisterNumber:212225240084
*/
import java.util.*;

public class Main {
    static int getMin(int[] arr, int i, int n) 
    {
        
        if (i == n - 1)
            return arr[i];
        
        int minRest = getMin(arr, i + 1, n);
        return Math.min(arr[i], minRest);
        
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for(int i=0; i<n; i++) {
            arr[i] = sc.nextInt();
        }
        System.out.println(getMin(arr, 0, n));
    }
}
```

## Output:
<img width="671" height="351" alt="image" src="https://github.com/user-attachments/assets/6e375cac-9113-4a10-9c81-e1d77eb97686" />



## Result:
Thus the JAVA prograM ti find the minimum value (e.g., lowest heartbeat), implement a recursive method has implemented successfully
