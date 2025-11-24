# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for set the priority and name of the current thread. Read the threadname from the User and Set the Priority as 2.

## AIM:
To Write a java program for set the priority and name of the current thread.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Get the current thread using Thread.currentThread().
4.	Set the thread’s name to the user-entered value.
5.	Set the priority of the thread to 2.
6.	Display the thread’s priority, name, and full thread information.
7.	End

## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: GOKULA PRIYA P
RegisterNumber:  212222040044
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        String threadName = sc.nextLine();
        Thread t = Thread.currentThread();
        t.setName(threadName);
        t.setPriority(2);
        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());
        System.out.println(t);
    }
}
```
## OUTPUT:
<img width="899" height="314" alt="image" src="https://github.com/user-attachments/assets/8fe2b29b-4d40-4593-af33-33aa485a6681" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.

