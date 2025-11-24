# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Print "Hello" and "World" alternately from two threads using synchronized blocks.

## AIM:
To Print "Hello" and "World" alternately from two threads using synchronized blocks.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a HelloWorldPrinter object that manages synchronized printing using a lock and a turn flag (helloTurn).
4.	Thread-1 is created to run printHello(n), which prints "Hello" but only when it is its turn.
5.	Thread-2 is created to run printWorld(n), which prints "World" but only when it is its turn.
6.	Both threads use wait() and notifyAll() to alternate printing without overlapping.
7.	Start both threads, resulting in output in the pattern
8.	End

## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: GOKULA PRIYA P
RegisterNumber:  212222040044
*/
```

## SOURCE CODE:
```
import java.util.*;
class HelloWorldPrinter {
    private final Object lock = new Object();
    private boolean helloTurn = true; // flag to alternate turns

    public void printHello(int n) {
        for (int i = 0; i < n; i++) {
            synchronized (lock) {
                while (!helloTurn) { // wait if it's not Hello's turn
                    try {
                        lock.wait();
                    } catch (InterruptedException e) {
                        Thread.currentThread().interrupt();
                    }
                }
                System.out.println("Hello");
                helloTurn = false;
                lock.notifyAll();
            }
        }
    }

    public void printWorld(int n) {
        for (int i = 0; i < n; i++) {
            synchronized (lock) {
                while (helloTurn) { // wait if it's not World's turn
                    try {
                        lock.wait();
                    } catch (InterruptedException e) {
                        Thread.currentThread().interrupt();
                    }
                }
                System.out.println("World");
                helloTurn = true;
                lock.notifyAll();
            }
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt(); // number of times to print
        HelloWorldPrinter printer = new HelloWorldPrinter();

        Thread t1 = new Thread(() -> printer.printHello(n));
        Thread t2 = new Thread(() -> printer.printWorld(n));

        t1.start();
        t2.start();
    }
}
```

## OUTPUT:
<img width="1073" height="763" alt="image" src="https://github.com/user-attachments/assets/a5059862-d7a5-410b-942f-4351ef9e5258" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.


