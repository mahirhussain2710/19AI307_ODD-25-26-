# Ex.No:3(C) ABSTRACTION

## QUESTION:
Description: Create abstract class GameScore with method finalScore(). Subclasses:

ArcadeGame: score = baseScore + (level × 100)

PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500

Input Format:

First line: 1 or 2 Second line: base, level (or attempts)

Output Format:

Final score (int)

For example:

Input Result 1 100 3 400 2 4 500

## AIM:
To develop a Java program demonstrating abstraction using an abstract class and method implementation in subclasses.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an abstract class with an abstract method.
4. Create subclasses and override the method.
5. Read user choice and inputs.
6. Instantiate appropriate subclass.
7. Call the overridden method.
8. Display the result.
9. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by:  MAHIR HUSSAIN S
RegisterNumber:  212223040109
*/
```

## SOURCE CODE:
```
import java.util.*;
abstract class GameScore
{
    abstract int finalScore();
    
}
class Aracade extends GameScore
{
    int base;
    int lev;
    Aracade(int base,int lev)
    {
        this.base=base;
        this.lev=lev;
    }
    @Override
    int finalScore()
    {
        return base+(lev*100);
    }
}
class Puzzle extends GameScore
{
    int att;
    Puzzle(int att)
    {
        this.att=att;
    }
    @Override
    int finalScore()
    {
        return (att<=3) ? 1000 - (att * 100) : 500;
    }
}
class prog
{
    public static void main(String [] args)
    {
        Scanner sc=new Scanner(System.in);
        int choice=sc.nextInt();
        if(choice==1)
        {
            int base=sc.nextInt();
            int lev=sc.nextInt();
            Aracade a=new Aracade(base,lev);
            System.out.println(a.finalScore());
        }
        else if(choice==2)
        {
            int att=sc.nextInt();
            Puzzle p=new Puzzle(att);
            System.out.println(p.finalScore());
        }
    }
}
```

## OUTPUT:
<img width="456" height="257" alt="image" src="https://github.com/user-attachments/assets/d35f2b3e-215b-4b00-b1ba-163c9b24d913" />

## RESULT:
The program was executed successfully and demonstrated abstraction with correct output.
