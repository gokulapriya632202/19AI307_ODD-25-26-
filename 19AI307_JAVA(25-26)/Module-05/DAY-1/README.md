# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to read user input from the keyboard using InputStreamReader 

## AIM:
To write a program to read user input from the keyboard using InputStreamReader 

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a single word (name) from the user using Scanner.
4.	Store the input in a string variable.
5.	Print the message "Hello, <name>!" using the stored value.
6.	End the program.

## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: GOKULA PRIYA P
RegisterNumber:  212222040044
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.*;
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        BufferedReader bf=new BufferedReader(new InputStreamReader(System.in));
        String str=sc.next();
        System.out.print("Hello, "+str+"!");
        
    }
}
```

## OUTPUT:
<img width="780" height="345" alt="image" src="https://github.com/user-attachments/assets/58c358ef-74ca-478a-b5db-415dcef3bf27" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.

