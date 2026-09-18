# Ex7 Priority Queue
## DATE:
## AIM:
To formulate the Java code to display the elements of the priority queue after insertion and deletion operation.

## Algorithm
1. Start the program.
2. Initialize a Priority Queue in Java using `PriorityQueue`.
3. Insert elements into the priority queue using `add()`.
4. Display the elements of the queue.
5. Delete elements using `poll()` and display the elements after deletion.
6. End the program.

## Program:
```java
// Program to display the elements of the priority queue after insertion and deletion operation
// Developed by: Surya Prakash B
// RegisterNumber: 212224230281

import java.util.PriorityQueue;

public class PQDemo {
    public static void main(String args[]) {
        PriorityQueue<Integer> pq = new PriorityQueue<Integer>();
        pq.add(10);
        pq.add(20);
        pq.add(15);
        
        System.out.println("Priority Queue after insertion: " + pq);
        System.out.println("Deleted element: " + pq.poll());
        System.out.println("Priority Queue after deletion: " + pq);
    }
}
```

## Output:
```text
Priority Queue after insertion: [10, 20, 15]
Deleted element: 10
Priority Queue after deletion: [15, 20]
```

## Result:
Thus, the Java program to display the elements of the priority queue after insertion and deletion operation is implemented successfully
