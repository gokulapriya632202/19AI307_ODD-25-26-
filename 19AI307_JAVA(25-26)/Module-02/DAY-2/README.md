# Ex.No:2(B) METHODS

## QUESTION:
Write a method void modifyValue(int num) that tries to modify the passed value(add passed value with 10) and print "Inside method: "+num . 
Show in main() that the original value does not change.
After calling modifyValue(int num) method in main , print the "Outside method: "+num

## AIM:
To create a method void and display the output.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Call the method modify(num).
4.	Inside the modify method: i) Receive the value of num as a parameter. ii.) Add 10 to this local copy of num.
5.	Return back to the main method.
6.	Print the original value of num as output.
7.	End

## PROGRAM:
 ```

Program to implement a Methods using Java
Developed by: GOKULA PRIYA P
RegisterNumber:  212222040044

```

## SOURCE CODE:
```
import java.util.*;
public class Main{
    static void modify(int num){
        num=num+10;
        System.out.println("Inside method: "+num);
    }
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        int num=sc.nextInt();
        modify(num);
        System.out.println("Outside method: "+num);
    }
}
```

## OUTPUT:
<img width="1234" height="286" alt="image" src="https://github.com/user-attachments/assets/069ba3c2-2eec-4a8b-b95a-ec15edb86521" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.

