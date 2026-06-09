# Ex.No:3(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.

Bot Types:

SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".

RainBot: Predicts "COLD" if temperature < 20, else "WARM".

Input:

temperature botType (1 for SunBot, 2 for RainBot)Output: Prediction as a string.

For example:

Input Result 35 1 HOT

## AIM:
To develop a Java program demonstrating the use of interfaces and implementing classes with runtime polymorphism.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an interface with a method.
4. Implement the interface in multiple classes.
5. Define logic inside each class.
6. Read input values.
7. Choose class based on input.
8. Call the implemented method.
9. Display the result.
10.Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by:  MAHIR HUSSAIN S
RegisterNumber:  212223040109
*/
```

## SOURCE CODE:
```
import java.util.*;
abstract class Temp
{
    abstract String Pred();
}
class Sunbot extends Temp
{
    int n;
    Sunbot(int n)
    {
        this.n=n;
    }
    @Override
    String Pred()
    {
        if(n>30)
        {
            return "HOT";
        }
        else 
        {
            return "MODERATE";
        }
    }
}
class Rainbot extends Temp
{
    int n;
    Rainbot(int n)
    {
        this.n=n;
    }
    @Override
    String Pred()
    {
        if(n<20)
        {
            return "COLD";
        }
        else 
        {
            return "WARM";
        }
    }
}
class prog
{
    public static void main(String [] args)
    {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();

        int choice=sc.nextInt();
        if(choice==1)
        {
            Sunbot s=new Sunbot(n);
            System.out.println(s.Pred());
        }
        else if(choice==2)
        {
            Rainbot r =new Rainbot(n);
            System.out.println(r.Pred());
        }
    }
}
```


## OUTPUT:
<img width="443" height="212" alt="image" src="https://github.com/user-attachments/assets/0221d641-175f-4c42-b032-5154095ebdb3" />


## RESULT:
The program was executed successfully and demonstrated interface implementation with correct output.
