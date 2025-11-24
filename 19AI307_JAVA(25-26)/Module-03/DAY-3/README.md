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
To develop a Java program using an abstract class to calculate final game scores for two game types: ArcadeGame and PuzzleGame.

## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the game type (1 or 2).
4.Create abstract class GameScore with abstract method finalScore().
5.If user enters 1, read baseScore and level.
   -> Calculate: score = baseScore + (level × 100)
6.If user enters 2, read attempts.
   -> If attempts ≤ 3, score = 1000 - (attempts × 100)
   -> Else, score = 500
7.Print the final score.
8.End program.
```




## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: Agalya R
RegisterNumber: 212222040003
*/
```

## SOURCE CODE:
```
import java.util.*;
abstract class GameScore
{
    abstract int finalScore();
}
class ArcadeGame extends GameScore
{
    int base,level;
    ArcadeGame(int base,int level)
    {
        this.base=base;
        this.level=level;
    }
    int finalScore()
    {
        return base+(level*100);
    }
    
}
class PuzzleGame extends GameScore
{
    int attempts;
    PuzzleGame(int attempts)
    {
        this.attempts=attempts;
    }
    int finalScore()
    {
        return (attempts<=3) ? 1000-(attempts*100):500;
    }
}
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        int type=sc.nextInt();
        GameScore game;
        if(type==1)
        {
            int base=sc.nextInt();
            int level=sc.nextInt();
            game=new ArcadeGame(base,level);
        }
        else
        {
            int attempts=sc.nextInt();
            game=new PuzzleGame(attempts);
        }
        System.out.println(game.finalScore());
    }
}
```






## OUTPUT:
<img width="1269" height="332" alt="image" src="https://github.com/user-attachments/assets/253cd93b-0b9a-4187-b30d-377c696770be" />



## RESULT:
The program successfully calculates the final score for Arcade and Puzzle games using an abstract class with overridden methods.

