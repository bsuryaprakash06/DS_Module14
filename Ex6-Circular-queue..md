# Ex6 Dequeue Elements from Circular Queue
## DATE: 18 - 08 - 2026
## AIM:
To write a Java program to delete three elements from the filled circular queue.

## Algorithm
1. Start the program.
2. Initialize a Circular Queue with a maximum size.
3. Insert elements into the queue until it is full.
4. Call the dequeue operation three times.
5. In each dequeue operation, check if the queue is empty.
6. If not empty, retrieve the element at the front, and increment front circularly.
7. Print the deleted elements and the state of the queue.
8. End the program.

## Program:
```java
// Program to delete three elements from the filled circular queue
// Developed by: Surya Prakash B
// RegisterNumber: 212224230281

import java.util.Scanner;

public class CircularQueue {
    int size;
    int front, rear;
    int[] queue;

    CircularQueue(int size) {
        this.size = size;
        this.front = this.rear = -1;
        this.queue = new int[size];
    }

    void enqueue(int data) {
        if ((front == 0 && rear == size - 1) || (rear == (front - 1) % (size - 1))) {
            System.out.println("Queue is Full");
        } else if (front == -1) {
            front = rear = 0;
            queue[rear] = data;
        } else if (rear == size - 1 && front != 0) {
            rear = 0;
            queue[rear] = data;
        } else {
            rear++;
            queue[rear] = data;
        }
    }

    int dequeue() {
        if (front == -1) {
            System.out.println("Queue is Empty");
            return -1;
        }
        int data = queue[front];
        if (front == rear) {
            front = -1;
            rear = -1;
        } else if (front == size - 1) {
            front = 0;
        } else {
            front++;
        }
        return data;
    }

    public static void main(String[] args) {
        CircularQueue cq = new CircularQueue(5);
        cq.enqueue(10);
        cq.enqueue(20);
        cq.enqueue(30);
        cq.enqueue(40);
        cq.enqueue(50);
        
        System.out.println("Deleted element: " + cq.dequeue());
        System.out.println("Deleted element: " + cq.dequeue());
        System.out.println("Deleted element: " + cq.dequeue());
    }
}
```

## Output:
```text
Deleted element: 10
Deleted element: 20
Deleted element: 30
```

## Result:
Thus, the Java program to delete three elements from the filled circular queue is implemented successfully.
