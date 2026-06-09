# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
Read 4 inputs, each expected to be an integer. If the input is not an integer, catch the exception and print "Invalid input".

## AIM:
To develop a Java program demonstrating exception handling for invalid user input.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read inputs from the user.
4. Use try-catch block.
5. Attempt to read integer values.
6. Catch exception if input is invalid.
7. Display appropriate message.
8. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by:  MAHIR HUSSAIN S
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
        for(int i=1;i<=4&& sc.hasNext();i++)
        {
            try
            {
                int n=sc.nextInt();
                System.out.println("Input accepted: "+n);
            }
            catch(InputMismatchException e)
            {
                System.out.println("Invalid input");
                sc.next();
            }
        }
        
    }
}
```


## OUTPUT:
<img width="732" height="352" alt="image" src="https://github.com/user-attachments/assets/7e97591a-6bd2-43a0-9f78-496456a36d81" />



## RESULT:
The program was executed successfully and handled invalid inputs using exception handling.
