# Ex10 Applications of Queue – FCFS
## DATE: 21 - 08 - 2026
## AIM:
To write a Java program to calculate the turnaround time of each process given their burst time and waiting time in First Come first Serve scheduling algorithm.

## Algorithm
1. Start the program.
2. Read the number of processes, their burst times, and waiting times.
3. Turnaround time is calculated as TAT[i] = BT[i] + WT[i].
4. Display the turnaround time for each process.
5. End the program.

## Program:
```java
// Program to calculate the turnaround time of each process in FCFS
// Developed by: Surya Prakash B
// RegisterNumber: 212224230281

import java.util.Scanner;

public class FCFS {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter number of processes: ");
        int n = sc.nextInt();
        int[] bt = new int[n];
        int[] wt = new int[n];
        int[] tat = new int[n];
        
        System.out.println("Enter Burst Time:");
        for(int i=0; i<n; i++) bt[i] = sc.nextInt();
        
        System.out.println("Enter Waiting Time:");
        for(int i=0; i<n; i++) wt[i] = sc.nextInt();
        
        System.out.println("Process\tBurst Time\tWaiting Time\tTurnaround Time");
        for(int i=0; i<n; i++) {
            tat[i] = bt[i] + wt[i];
            System.out.println((i+1) + "\t\t" + bt[i] + "\t\t\t" + wt[i] + "\t\t\t" + tat[i]);
        }
    }
}
```

## Output:
```text
Enter number of processes: 3
Enter Burst Time:
2 4 6
Enter Waiting Time:
0 2 6
Process Burst Time  Waiting Time    Turnaround Time
1       2           0               2
2       4           2               6
3       6           6               12
```

## Result:
Thus, the Java function to calculate the turnaround time of each process given their burst time and waiting time in First Come first Serve scheduling algorithm is implemented successfully.
