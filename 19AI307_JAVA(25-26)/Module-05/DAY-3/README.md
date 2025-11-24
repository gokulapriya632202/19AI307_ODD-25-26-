# Ex.No:5(C)  FILE HANDLING USING JAVA

## QUESTION:
Read a file and reverse the order of words in each line.

## AIM:
To Read a file and reverse the order of words in each line.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	For each line, stop the program if the input is "exit".
4.	Skip the line if it is empty.
5.	Split the line into words, reverse their order, and join them back into a sentence.
6.	Print the reversed sentence and continue until the user types "exit".
7.	End.

## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: GOKULA PRIYA P
RegisterNumber: 212222040044 

*/
```

## SOURCE CODE:
```
import java.util.*;

public class ReverseWordsInFile {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Reversed lines: ");
        while (sc.hasNextLine()) {
            String line = sc.nextLine();
            if (line.trim().equals("exit")) break;
            if (line.trim().isEmpty()) continue;
            String[] words = line.split("\\s+");
            StringBuilder reversed = new StringBuilder();
            for (int i = words.length - 1; i >= 0; i--) {
                reversed.append(words[i]);
                if (i != 0) reversed.append(" ");
            }
            System.out.println(reversed.toString());
        }
        sc.close();
    }
}
```

## OUTPUT:
<img width="1058" height="324" alt="image" src="https://github.com/user-attachments/assets/6b1307c6-601d-4fc1-b2ca-52d227e536b8" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.


