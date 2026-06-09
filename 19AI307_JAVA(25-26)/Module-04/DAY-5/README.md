# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Design a program where a Product model stores item info, and the view displays it. Implement a controller to update product price and refresh the view automatically.

## AIM:
To develop a Java program demonstrating separation of concerns using MVC architecture.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a model class to store data.
4. Create a view class to display data.
5. Create a controller class to update data.
6. Link model, view, and controller.
7. Modify data through controller.
8. Refresh view automatically.
9. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by:  MAHIR HUSSAIN S
RegisterNumber:  212223040109
*/
```

## SOURCE CODE:
```
import java.util.*;

// Model
class Product {
    private String name;
    private double price;
    private String code;

    public Product(String name, double price, String code) {
        this.name = name;
        this.price = price;
        this.code = code;
    }

    public String getName() {
        return name;
    }

    public double getPrice() {
        return price;
    }

    public String getCode() {
        return code;
    }

    public void setPrice(double price) {
        this.price = price;
    }
}

// View
class ProductView {
    public void displayProduct(Product product) {
        System.out.println("--- Product Details ---");
        System.out.println("Name : " + product.getName());
        System.out.println("Price: " + product.getPrice());
        System.out.println("Code : " + product.getCode());
    }
}

// Controller
class ProductController {
    private Product model;
    private ProductView view;

    public ProductController(Product model, ProductView view) {
        this.model = model;
        this.view = view;
    }

    public void updatePrice(double newPrice) {
        model.setPrice(newPrice);
        updateView();
    }

    public void updateView() {
        view.displayProduct(model);
    }
}

// Main
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String name = sc.nextLine();
        double price = Double.parseDouble(sc.nextLine());
        String code = sc.nextLine();
        double newPrice = Double.parseDouble(sc.nextLine());

        Product product = new Product(name, price, code);
        ProductView view = new ProductView();
        ProductController controller = new ProductController(product, view);

        // Display original
        controller.updateView();

        // Update price and display again
        controller.updatePrice(newPrice);

        sc.close();
    }
}
```


## OUTPUT:
<img width="783" height="383" alt="image" src="https://github.com/user-attachments/assets/1a856735-a573-4526-b85d-7b5c7ada4981" />


## RESULT:
The program was executed successfully and demonstrated MVC architecture with dynamic data updates.
