# Ex.No:3(E) INNER CLASS

## QUESTION:
Write an enum Grade with constants A, B, C, D, F. Assign a message like "Excellent" for A and "Good" for B and "Average" for C and "Fail" for F using constructor. Display grade with message.

## AIM:
To Write an enum Grade with constants A, B, C, D, F. Assign a message like "Excellent" for A and "Good" for B and "Average" for C and "Fail" for F using constructor. Display grade with message.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define an enum Grade with grade constants and messages for each.
4.	Try converting the input to the matching enum using valueOf().
5.	If valid, print the grade along with its message.
6.	If invalid, catch the exception and print “Invalid grade!”, then end the program.

## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: GOKULA PRIYA P
RegisterNumber:  212222040044
*/
```

## SOURCE CODE:
```
import java.util.*;

enum Grade {
    A("Excellent"),
    B("Good"),
    C("Average"),
    D("Poor"),
    F("Fail");

    private String message;

    Grade(String message) {
        this.message = message;
    }

    public String getMessage() {
        return message;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine().toUpperCase();

        try {
            Grade grade = Grade.valueOf(input);
            System.out.println("Grade: " + grade + " - " + grade.getMessage());
        } catch (IllegalArgumentException e) {
            System.out.println("Invalid grade!");
        }
    }
}
```
## OUTPUT:
<img width="1046" height="378" alt="image" src="https://github.com/user-attachments/assets/7efca0ee-9047-4145-8ff5-6e1678239d2b" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.

