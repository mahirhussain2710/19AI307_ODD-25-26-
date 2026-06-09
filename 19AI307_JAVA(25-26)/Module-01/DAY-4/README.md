# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java Program to Find the Average of Array Elements.

For example:

Input Result 5 10 20 30 40 50 The average of elements is 30.00

## AIM:
To develop a Java program to calculate the average of elements in an array.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the number of elements.
4. Store elements in an array.
5. Find the sum of all elements.
6. Calculate average = sum / number of elements.
7. Display the average.
8. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: MAHIR HUSSAIN S
RegisterNumber:  212223040109
*/
```

## SOURCE CODE:

```
import java.util.*;
class prog
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int [] arr=new int[n];
        int sum=0;
        for(int i=0;i<n;i++)
        {
            arr[i]=sc.nextInt();
            sum+=arr[i];
        }
        double avg=(double)sum/n;
        System.out.printf("The average of elements is %.2f",avg);
    }
}
```

## OUTPUT:

<img width="1023" height="605" alt="image" src="https://github.com/user-attachments/assets/39ef0204-bc69-420a-b202-67ad3ca6866c" />


## RESULT:
The program was executed successfully and the average of the array elements was displayed.
