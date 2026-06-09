# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
In a magical building, an elevator behaves oddly:

If the floor number is divisible by 3 and 5, it says "Skipped".

If the floor number is divisible by 3 only, it says "Beware!".

If the floor number is divisible by 5 only, it says "Blessings!".

Otherwise, it announces the floor number - print - "Floor {number}" .

Write a Java program to simulate this elevator logic for a given floor number.

For example:

Test Input Result t04 7 Floor 7

## AIM:
To develop a Java program using conditional statements to implement decision-making logic based on given numerical conditions.

## ALGORITHM :
1.Start the program.
2.Import the necessary package 'java.util'
3.Read the input value.
4.Use conditional statements to check given conditions.
5.Execute the corresponding output based on conditions.
6.Stop the program.

## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: MAHIR HUSSAIN S
RegisterNumber:  212223040109
*/
```

## SOURCE CODE:
```
import java.util.*;
public class prog
{
    public static void main(String [] args)
    {
        Scanner sc=new Scanner(System.in);
        int a=sc.nextInt();
        if(a%3==0 && a%5==0)
        {
            System.out.println("Skipped");
        }
        else if(a%3==0)
        {
            System.out.println("Beware!");
        }
        else if(a%5==0)
        {
            System.out.println("Blessings!");
        }
        else
        {
            System.out.println("Floor "+a);
        }
    }
}
```

## OUTPUT:
<img width="647" height="386" alt="image" src="https://github.com/user-attachments/assets/a5d212c6-3269-464e-bde7-157a8c546407" />



## RESULT:
The program was executed successfully and the output was displayed based on the given conditions.

