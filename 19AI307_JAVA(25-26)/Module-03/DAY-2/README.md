# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program to create a base class Animal (Animal Family) with a method called Sound(). Create two subclasses Bird and Cat. Override the Sound() method in each subclass to make a specific sound for each animal.

## AIM:
To write a Java program to create a base class Animal (Animal Family) with a method called Sound(). Create two subclasses Bird and Cat. Override the Sound() method in each subclass to make a specific sound for each animal.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a base class Animal with a method Sound() that prints a general message.
4.	Create subclasses Bird and Cat that override the Sound() method with specific sounds.
5.	In the main method, check the user input to determine which animal object to create.
6.	Call the Sound() method on the selected object to display the appropriate sound.
7.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: GOKULA PRIYA P
RegisterNumber:  212222040044
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Animal {
    void Sound() {
        System.out.println("Animal makes a sound");
    }
}

class Bird extends Animal {
    @Override
    void Sound() {
        System.out.println("Bird chirps");
    }
}

class Cat extends Animal {
    @Override
    void Sound() {
        System.out.println("Cat meows");
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String type = sc.next().toLowerCase();

        Animal animal;

        if (type.equals("bird")) {
            animal = new Bird();
        } else if (type.equals("cat")) {
            animal = new Cat();
        } else {
            animal = new Animal();
        }

        animal.Sound();
        sc.close();
    }
}
```
## OUTPUT:
<img width="1017" height="384" alt="image" src="https://github.com/user-attachments/assets/dd6609fa-4a0c-4989-af94-a275fc5bc657" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.


