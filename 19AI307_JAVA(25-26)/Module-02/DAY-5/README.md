# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Counter with a static integer variable count. Every time an object is created, increase count by 1. Print the total count using a static method

class Counter { static int count = 0; // Your Code Here }

class prog { public static void main(String[] args) { // Your Code Here } }

For example:

Result Total objects created: 7

## AIM:
To develop a Java program using a static variable and method to count the number of objects created.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Declare a static variable count.
4. Increment count in the constructor.
5. Create multiple objects.
6. Use a static method to display count.
7. Stop the program.


## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by:  MAHIR HUSSAIN S
RegisterNumber:  212223040109
*/
```

## SOURCE CODE:
```
import java.util.*;
class Counter
{
    static int count=0;
    Counter()
    {
        count++;
    }
    static void display()
    {
        System.out.println("Total objects created: "+count);
    }
}
class prog
{
    public static void main(String []args)
    {
        Scanner sc=new Scanner (System.in);
        for(int i=0;i<7;i++)
        {
            new Counter();
        }
        Counter.display();
    }
}
```


## OUTPUT:
<img width="802" height="212" alt="image" src="https://github.com/user-attachments/assets/b38205f6-2eec-4afb-8bbc-a48dafb33899" />



## RESULT:
The program was executed successfully and the total number of objects created was displayed.
