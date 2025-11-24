# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
Create animals from two regions: "Africa" and "Asia". Use Abstract Factory to create families of animals (Herbivore, Carnivore). Print the interaction result.

## AIM:
To create animals from two regions: "Africa" and "Asia". Use Abstract Factory to create families of animals (Herbivore, Carnivore). Print the interaction result.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the region name from the user (Africa or Asia).
4.	Select the correct factory based on the region using if-else.
5.	Create a Herbivore and a Carnivore using the chosen factory.
6.	Pass the Herbivore to the Carnivore’s eat() method to simulate the food chain.
7.	Display the result showing which carnivore eats which herbivore.
8.	End

## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: GOKULA PRIYA P
RegisterNumber:  212222040044
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

interface Herbivore {}
interface Carnivore {
    void eat(Herbivore h);
}

interface AnimalFactory {
    Herbivore createHerbivore();
    Carnivore createCarnivore();
}

class Wildebeest implements Herbivore {}
class Lion implements Carnivore {
    public void eat(Herbivore h) {
        System.out.println("Lion eats Wildebeest");
    }
}
class AfricaFactory implements AnimalFactory {
    public Herbivore createHerbivore() {
        return new Wildebeest();
    }
    public Carnivore createCarnivore() {
        return new Lion();
    }
}

class Deer implements Herbivore {}
class Tiger implements Carnivore {
    public void eat(Herbivore h) {
        System.out.println("Tiger eats Buffalo");
    }
}
class AsiaFactory implements AnimalFactory {
    public Herbivore createHerbivore() {
        return new Deer();
    }
    public Carnivore createCarnivore() {
        return new Tiger();
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String region = sc.nextLine().toLowerCase();
        AnimalFactory factory;

        if (region.equals("africa")) factory = new AfricaFactory();
        else if (region.equals("asia")) factory = new AsiaFactory();
        else {
            System.out.println("Invalid region");
            return;
        }

        Carnivore carn = factory.createCarnivore();
        Herbivore herb = factory.createHerbivore();
        carn.eat(herb);
    }
}
```
## OUTPUT:
<img width="878" height="386" alt="image" src="https://github.com/user-attachments/assets/c4209fc2-c9bb-4b1b-9297-4850d917c4d4" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.


