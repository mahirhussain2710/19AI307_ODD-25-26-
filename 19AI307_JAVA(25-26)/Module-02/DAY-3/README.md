# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Smartphone with private instance variables brand, model, and storageCapacity. Provide public getter and setter methods to access and modify these variables. Add a method called increaseStorage() that takes an integer value and increases the storageCapacity by that value.

## AIM:
To develop a Java program using encapsulation with private variables, getters, setters, and methods to modify data.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class with private variables.
4. Provide getter and setter methods.
5. Create a method to modify a variable.
6. Create an object and assign values using setters.
7. Call the method to update the value.
8. Display the updated details.
9. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: MAHIR HUSSAIN S
RegisterNumber:  212223040109
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Smartphone {
    private String brand;
    private String model;
    private int storageCapacity;

    
    public String getBrand() {
        return brand;
    }

    public String getModel() {
        return model;
    }

    public int getStorageCapacity() {
        return storageCapacity;
    }

    
    public void setBrand(String brand) {
        this.brand = brand;
    }

    public void setModel(String model) {
        this.model = model;
    }

    public void setStorageCapacity(int storageCapacity) {
        this.storageCapacity = storageCapacity;
    }

   
    public void increaseStorage(int value) {
        if (value > 0) {
            this.storageCapacity += value;
        }
    }

    
    public void display() {
        System.out.println("Brand: " + brand);
        System.out.println("Model: " + model);
        System.out.println("Updated Storage Capacity: " + storageCapacity + " GB");
        System.out.println("------------------------------");
    }
}
public class prog
{
    public static void main(String [] args)
    {
        Scanner sc=new Scanner(System.in);
        Smartphone phone =new Smartphone();
        phone.setBrand(sc.nextLine());
        phone.setModel(sc.nextLine());
        phone.setStorageCapacity(sc.nextInt());
        int extra=sc.nextInt();
        phone.increaseStorage(extra);
        phone.display();
        sc.close();
    }
}
```


## OUTPUT:

<img width="1241" height="567" alt="image" src="https://github.com/user-attachments/assets/9b5bd52c-d24b-4e3b-b599-3f64519e5a8d" />


## RESULT:
The program was executed successfully and the smartphone details with updated storage capacity were displayed correctly.
