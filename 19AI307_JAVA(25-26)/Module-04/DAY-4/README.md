# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You’re creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types

For example:

Input Result dark Dark Button created Dark Checkbox created

## AIM:
To develop a Java program demonstrating the Abstract Factory pattern for creating related objects without specifying their concrete classes.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create interfaces for product types.
4. Implement concrete classes for each variant.
5. Create an abstract factory interface.
6. Implement concrete factories for each theme.
7. Read user input.
8. Instantiate appropriate factory.
9. Create objects using factory methods.
10.Display results.
11.Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by:  MAHIR HUSSAIN S
RegisterNumber:  212223040109
*/
```

## SOURCE CODE:
```
import java.util.*;

interface Button {
    void create();
}

interface Checkbox {
    void create();
}

class DarkButton implements Button {
    public void create() {
        System.out.println("Dark Button created");
    }
}

class DarkCheckbox implements Checkbox {
    public void create() {
        System.out.println("Dark Checkbox created");
    }
}

class LightButton implements Button {
    public void create() {
        System.out.println("Light Button created");
    }
}

class LightCheckbox implements Checkbox {
    public void create() {
        System.out.println("Light Checkbox created");
    }
}

interface UIFactory {
    Button createButton();
    Checkbox createCheckbox();
}

class DarkThemeFactory implements UIFactory {
    public Button createButton() {
        return new DarkButton();
    }

    public Checkbox createCheckbox() {
        return new DarkCheckbox();
    }
}

class LightThemeFactory implements UIFactory {
    public Button createButton() {
        return new LightButton();
    }

    public Checkbox createCheckbox() {
        return new LightCheckbox();
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String theme = sc.nextLine();

        UIFactory factory;

        if (theme.equalsIgnoreCase("dark")) {
            factory = new DarkThemeFactory();
        } else if (theme.equalsIgnoreCase("light")) {
            factory = new LightThemeFactory();
        } else {
            System.out.println("Invalid theme");
            sc.close();
            return;
        }

        Button button = factory.createButton();
        Checkbox checkbox = factory.createCheckbox();

        button.create();
        checkbox.create();

        sc.close();
    }
}
```

## OUTPUT:
<img width="770" height="350" alt="image" src="https://github.com/user-attachments/assets/b10b8a39-2a25-4904-905d-769eec9729ce" />



## RESULT:
The program was executed successfully and demonstrated the Abstract Factory pattern with correct output.
