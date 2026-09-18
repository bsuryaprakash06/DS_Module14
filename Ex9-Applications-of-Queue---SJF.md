# Ex9 Applications of Queue - SJF
## DATE:
## AIM:
To incorporate the Java code to calculate the Total Waiting Time and Average Waiting Time in Shortest Job First scheduling algorithm.

## Algorithm
1. Start the program.
2. Read the number of processes and their burst times.
3. Sort the processes based on their burst times in ascending order.
4. Calculate waiting time for each process: WT[i] = WT[i-1] + BT[i-1] with WT[0] = 0.
5. Calculate total waiting time by summing up the waiting times.
6. Calculate average waiting time.
7. End the program.

## Program:
```java
// Program to calculate the Total Waiting Time and Average Waiting Time in Shortest Job First scheduling algorithm
// Developed by: Surya Prakash B
// RegisterNumber: 212224230281

import java.util.Arrays;
import java.util.Scanner;

public class SJF {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter number of processes: ");
        int n = sc.nextInt();
        int[] bt = new int[n];
        System.out.println("Enter Burst Time:");
        for(int i=0; i<n; i++) {
            bt[i] = sc.nextInt();
        }
        
        Arrays.sort(bt);
        
        int wt = 0;
        int total_wt = 0;
        for(int i=1; i<n; i++) {
            wt += bt[i-1];
            total_wt += wt;
        }
        
        System.out.println("Total Waiting Time = " + total_wt);
        System.out.println("Average Waiting Time = " + (float)total_wt/n);
    }
}
```

## Output:
```text
Enter number of processes: 3
Enter Burst Time:
5 2 8
Total Waiting Time = 9
Average Waiting Time = 3.0
```

## Result:
Thus, the Java code to calculate the Total Waiting Time and Average Waiting Time in Shortest Job First scheduling algorithm is implemented successfully.
