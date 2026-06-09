# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
In mathematics, the factorial of a non-negative integer n, denoted as n!, is the product of all positive integers less than or equal to n. For example:

5! = 5 × 4 × 3 × 2 × 1 = 120

3! = 3 × 2 × 1 = 6

0! is defined as 1.

Write a Java program that prompts the user to enter a non-negative integer and then calculates and displays the factorial of the given number.

Use a for loop to perform the calculation.

Make sure to handle the case when the user enters 0.

Display the result in a clear and user-friendly way.

For example:

Input Result 0 Factorial of 0 is: 1

## AIM:
To develop a Java program using a loop to compute the factorial of a given non-negative integer.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a non-negative integer from the user.
4. Initialize a variable fact = 1.
5. Use a for loop from 1 to the given number.
6. Multiply fact with each number in the loop.
7. If the number is 0, set fact = 1.
8. Display the factorial result.
9. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: MAHIR HUSSAIN S
RegisterNumber:  212223040109
*/
```

## SOURCE CODE:
```
import java.util.*;
class prog
{
    public static void main(String [] args)
    {
        Scanner sc=new Scanner(System.in);
        int a=sc.nextInt();
        int ans=1;
        for(int i=1;i<=a;i++)
        {
            ans=ans*i;
        }
        System.out.println("Factorial of "+(a)+" is: "+(ans));
    }
}
```

## OUTPUT:
<img width="1036" height="342" alt="image" src="https://github.com/user-attachments/assets/d8bccdbd-5e04-422f-a5b0-3070931afa8c" />


## RESULT:
The program was executed successfully and the factorial of the given number was displayed correctly.
