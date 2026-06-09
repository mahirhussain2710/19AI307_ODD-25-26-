# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program to create a class MaxFinder with three overloaded max() methods:

max(int a, int b) – returns the maximum of two integers.

max(double a, double b) – returns the maximum of two double values.

max(int a, int b, int c) – returns the maximum of three integers.

In the main() method, demonstrate the use of each overloaded method with various inputs.

For example:

Input Result 10 20 3.5 2.8 7 12 9 Max(10, 20): 20 Max(3.5, 2.8): 3.5 Max(7, 12, 9): 12

## AIM:
To develop a Java program demonstrating compile-time polymorphism using method overloading.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define multiple methods with same name but different parameters.
4. Read input values.
5. Call appropriate method based on arguments.
6. Display the result.
7. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: MAHIR HUSSAIN S
RegisterNumber:  212223040109
*/
```

## SOURCE CODE:
```
import java.util.*;
class Maxfind
{
    int a;
    int b;
    double d1;
    double d2;
    int x;
    int y;
    int z;
    int max(int a,int b)
    {
        return Math.max(a,b);
    }
    double max(double d1,double d2)
    {
        return Math.max(d1,d2);
    }
    int max(int x,int y,int z)
    {
        return Math.max(Math.max(x,y),z);
    }
}
class prog
{
    public static void main(String [] args)
    {
        Scanner sc=new Scanner(System.in);
        int a=sc.nextInt();
        int b=sc.nextInt();
        double d1=sc.nextDouble();
        double d2=sc.nextDouble();
        int x=sc.nextInt();
        int y=sc.nextInt();
        int z=sc.nextInt();
        Maxfind m=new Maxfind();
        System.out.println("Max("+a+", "+b+"): "+m.max(a,b));
        System.out.println("Max("+d1+", "+d2+"): "+m.max(d1,d2));
        System.out.println("Max("+x+", "+y+", "+z+"): "+m.max(x,y,z));
    }
}
```

## OUTPUT:
<img width="890" height="492" alt="image" src="https://github.com/user-attachments/assets/0a6fef5b-987f-4cde-a1e8-e8a1b853e0ff" />

## RESULT:
The program was executed successfully and demonstrated method overloading.
