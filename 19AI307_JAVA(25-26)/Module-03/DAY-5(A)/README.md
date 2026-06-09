# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program where the inner class is declared private and accessed through a method in the outer class.

Input Result 3 Data set inside private inner class: 3

## AIM:
To develop a Java program demonstrating the use of a private inner class and accessing it through a method of the outer class.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an outer class.
4. Declare a private inner class inside it.
5. Define a method in the inner class.
6. Create a method in outer class to access inner class.
7. Read input value.
8. Call outer class method to display result.
9. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: MAHIR HUSSAIN S
RegisterNumber:  212223040109
*/
```

## SOURCE CODE:
```
import java.util.*;

class Outer {

    
    private class Inner {
        int data;

        Inner(int data) {
            this.data = data;
        }

        void display() {
            System.out.println("Data set inside private inner class: " + data);
        }
    }

    
    public void setData(int value) {
        Inner obj = new Inner(value);
        obj.display();
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int input = sc.nextInt();

        Outer outer = new Outer();
        outer.setData(input);
    }
}
```


## OUTPUT:
<img width="1147" height="290" alt="image" src="https://github.com/user-attachments/assets/6aa94a9d-19fd-41ce-b7a9-3e9199869c7f" />

## RESULT:
The program was executed successfully and demonstrated access to a private inner class through the outer class.
