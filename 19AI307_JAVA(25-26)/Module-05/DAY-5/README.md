# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Create a program that reads a thread name and a priority (1–10), sets that priority to a new thread, prints both values.

Input:

Two lines: ,

Output:

Thread priority set to

For example:

Input Result Alpha 5 Thread Alpha priority is 5

## AIM:
To set and display the name and priority of a thread based on user input.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read thread name from the user.
4. Read thread priority (1–10) from the user.
5. Create a thread.
6. Set the thread’s name and priority.
7. Display the thread’s name and priority.

## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by:  MAHIR HUSSAIN S
RegisterNumber:  212223040109
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class MyThread extends Thread {
    public MyThread(String name) {
        super(name); // set thread name
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String threadName = sc.nextLine();

        int priority = sc.nextInt();

        MyThread t = new MyThread(threadName);

        t.setPriority(priority);

        System.out.println("Thread " + t.getName() + " priority is " + t.getPriority());

        sc.close();
    }
}
```

## OUTPUT:
<img width="952" height="383" alt="image" src="https://github.com/user-attachments/assets/b9fdd804-ad71-4efd-8f2f-d1b1559df97d" />


## RESULT:
Thus the program successfully sets and displays the thread name and its priority.
