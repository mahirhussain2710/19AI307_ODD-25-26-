# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely is learning java basics, can you teach her the different types of datatypes in java? Write a program that uses all datatypes and print them all.

Input Format:

byte - 24

short - 11000

int - 1,34,500

long - 24,23,10,34

float - 24.20

double - 1,30,000.80

boolean - true/false

char - 'u'

String -"Heyyy, Lovely, Let's learn java!"

## AIM:
To develop a Java program that demonstrates the use of different data types and displays their values.

## ALGORITHM :
1.	Start the program.
2.	Declare variables of different data types.
3.	Assign given values to each variable.
4.	Use output statements to display all values.
5.	Stop the program.

## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: MAHIR HUSSAIN S
RegisterNumber:  212223040109
*/
```

## Sourcecode.java:
```
import java.util.*;
public class prog
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        byte b=sc.nextByte();
        short s=sc.nextShort();
        int i=sc.nextInt();
        long l=sc.nextLong();
        float f=sc.nextFloat();
        double d=sc.nextDouble();
        boolean bo=sc.nextBoolean();
        char c=sc.next().charAt(0);
        String str=sc.next();
        System.out.println("Hey Lovely, let's print all types of data received from user using different data types");
        System.out.println("This is byte datatype "+b);
        System.out.println("This is short datatype "+s);
        System.out.println("This is int datatype "+i);
        System.out.println("This is long datatype "+l);
        System.out.println("This is float datatype "+f);
        System.out.println("This is double datatype "+d);
        System.out.println("This is boolean datatype "+bo);
        System.out.println("This is char datatype "+c);
        System.out.println("This is string datatype "+str);
    }
}
```


## OUTPUT:
<img width="1253" height="660" alt="image" src="https://github.com/user-attachments/assets/ed1b88aa-d932-4432-9986-a8a39b425b76" />



## RESULT:
The program was executed successfully and all the data type values were displayed.
