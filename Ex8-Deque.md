# Ex8 Deque
## DATE:
## AIM:
To write a Java program to count the number of elements present in the deque.

## Algorithm
1. Start the program.
2. Initialize a Deque using `ArrayDeque`.
3. Add elements to the Deque using `addFirst()` and `addLast()`.
4. Use the `size()` method to count the number of elements present in the deque.
5. Print the count.
6. End the program.

## Program:
```java
// Program to count the number of elements present in the deque
// Developed by: Surya Prakash B
// RegisterNumber: 212224230281

import java.util.ArrayDeque;
import java.util.Deque;

public class DequeDemo {
    public static void main(String[] args) {
        Deque<Integer> deque = new ArrayDeque<Integer>();
        deque.addFirst(10);
        deque.addLast(20);
        deque.addFirst(5);
        
        System.out.println("Deque: " + deque);
        System.out.println("Number of elements: " + deque.size());
    }
}
```

## Output:
```text
Deque: [5, 10, 20]
Number of elements: 3
```

## Result:
Thus, the Java code to count the number of elements present in the deque is implemented successfully.
