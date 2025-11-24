# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create abstract class GameScore with method finalScore().
Subclasses:
ArcadeGame: score = baseScore + (level × 100)
PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500

## AIM:
To Create abstract class GameScore with method finalScore().


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define an abstract class GameScore with an abstract method finalScore().
4.	Create the ArcadeGame class that calculates the final score using baseScore + (level × 100).
5.	Create the PuzzleGame class that calculates the final score based on number of attempts.
6.	In main, if the user selects choice 1, read baseScore and level, and create an ArcadeGame object.
7.	If the user selects choice 2, read attempts and create a PuzzleGame object.
8.	Call the finalScore() method on the created object, print the result, and end the program.

## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: GOKULA PRIYA P
RegisterNumber: 212222040044
*/
```

## SOURCE CODE:
```
import java.util.*;

abstract class GameScore {
    abstract int finalScore();
}

class ArcadeGame extends GameScore {
    int baseScore, level;
    
    ArcadeGame(int baseScore, int level) {
        this.baseScore = baseScore;
        this.level = level;
    }

    int finalScore() {
        return baseScore + (level * 100);
    }
}

class PuzzleGame extends GameScore {
    int attempts;
    
    PuzzleGame(int attempts) {
        this.attempts = attempts;
    }

    int finalScore() {
        if (attempts <= 3)
            return 1000 - (attempts * 100);
        else
            return 500;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int choice = sc.nextInt();

        if (choice == 1) {
            int base = sc.nextInt();
            int level = sc.nextInt();
            GameScore game = new ArcadeGame(base, level);
            System.out.println(game.finalScore());
        } else if (choice == 2) {
            int attempts = sc.nextInt();
            GameScore game = new PuzzleGame(attempts);
            System.out.println(game.finalScore());
        }
        sc.close();
    }
}
```

## OUTPUT:
<img width="1026" height="349" alt="image" src="https://github.com/user-attachments/assets/0ce49387-e4e7-4c5f-bc56-96be4c94bb0b" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.


