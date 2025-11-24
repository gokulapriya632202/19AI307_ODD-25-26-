# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
If an Integer object is set to null, and you attempt to call .toString() on it, what happens? How can you prevent your code from throwing an exception in such cases?

## AIM:
To understand what happens when .toString() is called on a null Integer object in Java, identify the exception thrown, and learn how to prevent the exception by applying a null-check or using safe coding practices.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Input an Integer value or set the Integer reference.
4.	Check if the Integer object is null.
5.	If null, display "Null Integer" and stop processing.
6.	If not null, safely call .toString() on the Integer object.
7.	Display the converted string value.
8.	End
   
## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: GOKULA PRIYA P
RegisterNumber:  212222040044
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        
        try
        {
            Integer s=sc.nextInt();
            if(s==null || s==0){
                throw new NullPointerException();
            }
            else{
                System.out.println(s.toString());
            }
        }
        catch(Exception e)
        {
            System.out.println("Null Integer");
        }
    }
}
```
## OUTPUT:
<img width="1194" height="430" alt="image" src="https://github.com/user-attachments/assets/41649df3-eb80-4f70-a80d-807e0fdc3f06" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.


