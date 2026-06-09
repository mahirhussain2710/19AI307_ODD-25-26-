# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a program to overwrite the content of a file.

For example:

Input Result Saveetha Engineering College File content overwritten successfully.

## AIM:
To develop a Java program to overwrite the content of a file using character stream.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read input content.
4. Create FileWriter object in overwrite mode.
5. Write new content to the file.
6. Close the file.
7. Display success message.
8. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by:  MAHIR HUSSAIN S
RegisterNumber:  212223040109
*/
```

## SOURCE CODE:
```
import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String content = sc.nextLine();

        String filename = "output.txt"; // file name

        try {
            FileWriter writer = new FileWriter(filename);

            writer.write(content); // overwrite content
            writer.close();

            System.out.println("File content overwritten successfully.");
        } catch (IOException e) {
            System.out.println("Error: " + e.getMessage());
        }

        sc.close();
    }
}
```


## OUTPUT:
<img width="1261" height="232" alt="image" src="https://github.com/user-attachments/assets/e135c40f-66b6-4ede-bd3e-58f84512d959" />

## RESULT:
The program was executed successfully and the file content was overwritten.
