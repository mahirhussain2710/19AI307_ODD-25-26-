# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to demonstrate chaining of streams (BufferedReader on top of InputStreamReader on top of System.in)

Input Result Ram 25 --- User Details --- Name: Ram Age: 25

## AIM:
To develop a Java program demonstrating chaining of input streams for efficient data reading.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an InputStreamReader object.
4. Wrap it with BufferedReader.
5. Read input values.
6. Process the input.
7. Display the result.
8. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by:  MAHIR HUSSAIN S
RegisterNumber:  212223040109
*/
```

## SOURCE CODE:
```
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class ChainingStreamsExample {
    public static void main(String[] args) {
        // Chaining: System.in -> InputStreamReader -> BufferedReader


       //Write your code here
       try
       {
           BufferedReader br=new BufferedReader(new InputStreamReader(System.in));
           String name=br.readLine();
           int age=Integer.parseInt(br.readLine());
           System.out.println("--- User Details ---");
           System.out.println("Name: "+name);
           System.out.println("Age: "+age);
       }
       catch(IOException e)
       {
               System.out.println("Error reading input");
           
       }
    }
}

```


## OUTPUT:
<img width="763" height="592" alt="image" src="https://github.com/user-attachments/assets/8e9f3058-d1f7-46cf-b47d-e13f85ff75cf" />

## RESULT:
The program was executed successfully and demonstrated stream chaining with correct output.
