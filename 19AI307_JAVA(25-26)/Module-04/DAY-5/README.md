# Ex.No:4(E) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Design a program where a Product model stores item info, and the view displays it. Implement a controller to update product price and refresh the view automatically.

## AIM:
To implement a behavioral design pattern in Java using Model–View–Controller (MVC), where the controller updates the model and refreshes the view dynamically.


## ALGORITHM :
1. Start the program and read product details from the user.
2. Create a Product model class to store name, price, and code.
3. Create a ProductView class to display product details.
4. Create a ProductController class to modify price and update the view.
5. Display product details before and after price update, then end the program.

## PROGRAM:
```txt
Program to implement a Behaviour Pattern using Java
Developed by: Sudharsanam R K
RegisterNumber: 212222040163
```

## SOURCE CODE:
```java
import java.util.Scanner;

public class ProductManagementSystem {

    static class Product {
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

    static class ProductView {
        public void displayProduct(String name, double price, String code) {
            System.out.println("--- Product Details ---");
            System.out.println("Name : " + name);
            System.out.println("Price: " + price);
            System.out.println("Code : " + code);
        }
    }

    static class ProductController {
        private Product product;
        private ProductView view;

        public ProductController(Product product, ProductView view) {
            this.product = product;
            this.view = view;
        }

        public void updateView() {
            view.displayProduct(product.getName(), product.getPrice(), product.getCode());
        }

        public void updatePrice(double newPrice) {
            product.setPrice(newPrice);
            updateView();
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String name = sc.nextLine();
        double price = sc.nextDouble();
        sc.nextLine(); 
        String code = sc.nextLine();
        double newPrice = sc.nextDouble();

        
        Product product = new Product(name, price, code);
        ProductView view = new ProductView();
        ProductController controller = new ProductController(product, view);

        controller.updateView();

        controller.updatePrice(newPrice);

        sc.close();
    }
}
```

## OUTPUT:
<img width="614" height="315" alt="image" src="https://github.com/user-attachments/assets/a0b3a036-d827-4f64-9235-374ffa0fa1eb" />

## RESULT:
The program successfully implemented a behavioral design pattern using MVC, where the controller updates product price and automatically refreshes the view.



