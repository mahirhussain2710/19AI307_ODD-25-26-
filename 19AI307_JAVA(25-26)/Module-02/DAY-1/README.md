# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Car with attributes brand, model, year. Create 2 objects and print their details.

For example:

Result Car 1: Toyota Innova 2022 Car 2: Hyundai i20 2021

## AIM:
To develop a Java program using a class and objects to store and display details.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class with required attributes.
4. Create objects of the class.
5. Assign values to the objects.
6. Display the object details.
7. Stop the program.


## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by:  MAHIR HUSSAIN S
RegisterNumber:  212223040109
*/
```

## SOURCE CODE:
```
class Car
{
    String brand, model;
    int year;
}
    

public class prog {
    public static void main(String[] args) {
        Car c1 = new Car();
        c1.brand = "Toyota";
        c1.model = "Innova";
        c1.year = 2022;

        Car c2 = new Car();
        c2.brand = "Hyundai";
        c2.model = "i20";
        c2.year = 2021;

        System.out.println("Car 1: " + c1.brand + " " + c1.model + " " + c1.year);
        System.out.println("Car 2: " + c2.brand + " " + c2.model + " " + c2.year);
        
        
    }
    
}


```

## OUTPUT:
<img width="848" height="227" alt="image" src="https://github.com/user-attachments/assets/266db0df-0b0a-4be4-9956-305e8410117f" />

## RESULT:
The program was executed successfully and the details of both car objects were displayed correctly.
