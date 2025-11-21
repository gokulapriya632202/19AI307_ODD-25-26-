# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Write a Java program to calculate the factorial of a number using a for loop. The factorial of n is the product of all positive integers less than or equal to n.

## AIM:
To write a Java program to calculate the factorial of a number using a for loop

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read an integer value num from the user.
4.	Initialize a variable fact = 1.
5.	Repeat the following steps for i = 1 to num and Multiply fact = fact × i.
6.	After the loop ends, fact will contain the factorial of the number.
7.	End

## PROGRAM:
 ```
Program to implement a Looping Statement using Java
Developed by: GOKULA PRIYA P
RegisterNumber:  212222040044

```

## SOURCE CODE:
```
import java.util.*;
class prog{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        int num=sc.nextInt();
        int fact=1;
        for(int i=1;i<=num;i++){
            fact=fact*i;
        }
        System.out.print("Factorial of "+num+" is: "+fact);
    }
}
```
## OUTPUT:
<img width="1288" height="351" alt="image" src="https://github.com/user-attachments/assets/99fc0123-68eb-4f6b-b892-864863e39934" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.


