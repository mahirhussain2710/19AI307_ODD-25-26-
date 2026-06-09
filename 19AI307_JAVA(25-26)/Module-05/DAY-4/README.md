# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for determine the priority and name of the current thread.

Note : Read the threadname from the User

For example:

Input Result NewThread Priority of Thread: 5 Name of Thread: NewThread Thread[NewThread,5,main]

## AIM:
To develop a Java program demonstrating thread creation and accessing thread properties.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read thread name from user.
4. Get current thread reference.
5. Set thread name.
6. Get thread priority.
7. Display thread details.
8. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by:  MAHIR HUSSAIN S
RegisterNumber:  212223040109
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String threadName = sc.nextLine();

        Thread t = Thread.currentThread();

        t.setName(threadName);

        t.setPriority(Thread.NORM_PRIORITY);

        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());
        System.out.println(t);

        sc.close();
    }
}
```

## OUTPUT:
<img width="906" height="252" alt="image" src="https://github.com/user-attachments/assets/9deb615f-c0a1-4424-b615-4ac1b610e39e" />


## RESULT:
The program was executed successfully and displayed the thread name and priority.
