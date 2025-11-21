# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Develop a class with a static nested class. 

<img width="654" height="156" alt="image" src="https://github.com/user-attachments/assets/1a0a4dfd-6039-4b0b-ac1a-a0a8769a7701" />

## AIM:
To Develop a class with a static nested class. 


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a static nested class containing the method display().
4.	Inside display(), create a Scanner object to read input.
5.	Print the static variable directly from the outer class.
6.	Create an object of the outer class and print its instance variable.
7.	Read a local variable from the user and print it.
8.	End.

## PROGRAM:
 ```

Program to implement a Variable scope and Constructor using Java
Developed by: GOKULA PRIYA P
RegisterNumber: 212222040044

```

## SOURCE CODE:
```
import java.util.*;
public class prog{
    static int staticvar=100;
    int instancevar=200;
    static class nestedclass{
        void display(){
            Scanner s=new Scanner(System.in);
            System.out.println("Accessing static variable from outer class: "+staticvar);
            prog outer=new prog();
            System.out.println("Accessing instance variable from outer class using object: "+outer.instancevar);
            int localvar=s.nextInt();
            System.out.println("Local variable inside nested class method: "+localvar);
            
        }
    }
    public static void main(String[] args){
        prog.nestedclass nested=new prog.nestedclass();
        nested.display();
    }
}
```

## OUTPUT:
<img width="1264" height="438" alt="image" src="https://github.com/user-attachments/assets/3299ba9c-4463-4131-8f2d-26f14eed20e6" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.


