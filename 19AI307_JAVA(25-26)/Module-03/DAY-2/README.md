# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program that calculates the area of different shapes using method overloading. Create a class AreaCalculator with:
- area(int side) for square
- area(int length, int breadth) for rectangle
- area(double radius) for circle
- For example:

| Input                | Result                                              |
|----------------------|------------------------------------------------------|
| 4 <br>5 6 <br>3.0    | Area of square: 16 <br>Area of rectangle: 30 <br>Area of circle: 28.274333882308138 |



## AIM:
To write a Java program that demonstrates method overloading by calculating the area of a square, rectangle, and circle using overloaded area() methods.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the side of a square, length, breadth, and radius from the user.
4. Create an object of the areacalc class.
5. Call the overloaded area(int) method to compute the area of a square.
6. Call the overloaded area(int,int) method to compute the area of a rectangle.
7. Call the overloaded area(double) method to compute the area of a circle and display all results.

## PROGRAM:
```txt
Program to implement a Polymorphism using Java
Developed by: Sudharsanam R K
RegisterNumber:212222040163
```

## SOURCE CODE:
```java
import java.util.*;
class areacalc {
    int area(int side) {    
    return side*side;
    }
    int area(int len,int breath) {
        return len*breath;
    }
    double area(double radius) {
        return Math.PI*radius*radius;
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner input=new Scanner(System.in);
        int side=input.nextInt();
        int len=input.nextInt();
        int breath=input.nextInt();
        double radius=input.nextDouble();
        
        areacalc calc=new areacalc();
        
        System.out.println("Area of square: "+calc.area(side));
        System.out.println("Area of rectangle: "+calc.area(len,breath));
        System.out.println("Area of circle: "+calc.area(radius));
    }
}
```

## OUTPUT:

## RESULT:
The program successfully demonstrates method overloading by calculating and displaying the areas of a square, rectangle, and circle using three versions of the area() method.

