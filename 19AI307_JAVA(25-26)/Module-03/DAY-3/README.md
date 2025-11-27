# Ex.No:3(C) ABSTRACTION

## QUESTION:
Description:
Create abstract class GameScore with method finalScore().
Subclasses:

ArcadeGame: score = baseScore + (level × 100)

PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500

Input Format:

First line: 1 or 2
Second line: base, level (or attempts)

Output Format:

Final score (int)

## AIM:
To calculate the final game score using abstraction and overridden methods for different game types.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an abstract class GameScore with an abstract method finalScore().
4.	Define ArcadeGame class that computes final score using base score and level.
5.	Define PuzzleGame class that computes final score based on number of attempts.
6.	Read the game type and input values from the user.
7.	Create the appropriate object and display its final score by calling finalScore().





## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber:  212222240008
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
        int type = sc.nextInt();
        if (type == 1) {
            int base = sc.nextInt();
            int level = sc.nextInt();
            GameScore g = new ArcadeGame(base, level);
            System.out.println(g.finalScore());
        } else if (type == 2) {
            int attempts = sc.nextInt();
            GameScore g = new PuzzleGame(attempts);
            System.out.println(g.finalScore());
        }
        sc.close();
    }
}
```




## OUTPUT:

<img width="461" height="324" alt="image" src="https://github.com/user-attachments/assets/48340e7a-ae2c-49cb-98a1-500869e60a95" />


## RESULT:
The program successfully computes and displays the final score for both Arcade and Puzzle games using abstraction and method overriding.
