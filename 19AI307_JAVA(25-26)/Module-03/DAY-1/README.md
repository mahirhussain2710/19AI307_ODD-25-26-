# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
Create a Super class Person with fields name and age. Create a subclass Student that inherits from Person and adds a field marks (integer). Implement a method in Student called calculateGrade() which returns the grade based on the marks:

Marks ≥ 90: Grade A

Marks ≥ 75 and < 90: Grade B

Marks ≥ 50 and < 75: Grade C

Marks < 50: Grade F


## AIM:
To develop a Java program demonstrating inheritance and method implementation.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a superclass with required fields.
4. Create a subclass that inherits the superclass.
5. Add additional field in subclass.
6. Implement method using conditional statements.
7. Create object and assign values.
8. Call method and display result.
9. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: MAHIR HUSSAIN S
RegisterNumber:  212223040109
*/
```

## SOURCE CODE:
```
import java.util.*;
class Person
{
    String name;
    int age;
    Person(String name,int age)
    {
        this.name=name;
        this.age=age;
    }
}
class Student extends Person
{
    int marks;
    Student(String name,int age,int marks)
    {
        super(name,age);
        this.marks=marks;
    }
    char calGrade()
    {
        if(marks>=90)
        {
            return 'A';
        }
        else if(marks>=75 && marks<90)
        {
            return 'B';
        }
        else if(marks>=50 && marks<75)
        {
            return 'C';
        }
        else
        {
            return 'F';
        }
    }
}
class prog
{
    public static void main(String []args)
    {
        Scanner sc=new Scanner(System.in);
        String name=sc.nextLine();
        int age=sc.nextInt();
        int marks=sc.nextInt();
        Student s=new Student(name,age,marks);
        System.out.println("Name: "+s.name);
        System.out.println("Age: "+s.age);
        System.out.println("Marks: "+s.marks);
        System.out.println("Grade: "+s.calGrade());
        sc.close();
    }
}
```

## OUTPUT:
<img width="665" height="713" alt="image" src="https://github.com/user-attachments/assets/9d01b24b-8af8-48ae-9ba8-20138fe8b975" />


## RESULT:
The program was executed successfully and the grade was calculated based on the marks.
