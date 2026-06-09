# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a class that uses a constructor to initialize variables and overrides toString() method.

nput Result Ram 20 Student{name='Ram', age=20}

## AIM:
To develop a Java program using a constructor to initialize variables and override the toString() method.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class with variables.
4. Define a constructor to initialize variables.
5. Override the toString() method.
6. Create an object and pass values.
7. Print the object.
8. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: MAHIR HUSSAIN S
RegisterNumber:  212223040109
*/
```

## SOURCE CODE:

```
import java.util.*;
class Student
{
    String name;
    int age;
    Student(String name,int age)
    {
        this.name=name;
        this.age=age;
    }
    public String toString()
    {
        return "Student{name='"+name+"', age="+age+"}";
    }
}
class prog
{
    public static void main(String [] args)
    {
        Scanner sc=new Scanner(System.in);
        String name=sc.nextLine();
        int age=sc.nextInt();
        Student s=new Student(name , age);
        System.out.println(s);
        sc.close();
    }
}
```


## OUTPUT:
<img width="955" height="397" alt="image" src="https://github.com/user-attachments/assets/0d0b87e2-38b6-44ea-8064-53796f1232ad" />



## RESULT:
The program was executed successfully and the object details were displayed using the overridden toString() method.
