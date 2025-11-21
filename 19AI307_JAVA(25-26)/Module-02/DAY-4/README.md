# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a program to access a static variable using both class name and object.

**Input:** 48

**Result:**

Accessing using class name: 48

Accessing using object: 48

## AIM:
To write a Java program that demonstrates variable scope by accessing a static variable using both class name and object reference.

## ALGORITHM :
1. Start the program.
2. Import the necessary package java.util.
3. Declare a static variable inside the class.
4. In the main method, get input from the user and store it in the static variable.
5. Access and print the static variable using the class name.
6. Create an object of the class.
7. Access and print the static variable using the object.
8. End the program.

## PROGRAM:
```
Program to implement a Variable scope and Constructor using Java
Developed by: Sudharsanam R K
RegisterNumber: 212222040163
```

## SOURCE CODE:
```java
import java.util.*;
public class prog { 
    static int val;

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        prog.val = input.nextInt();

        System.out.println("Accessing using class name: " + prog.val);

        prog obj = new prog();
        System.out.println("Accessing using object: " + obj.val);
    }
}
```

## OUTPUT:
<img width="733" height="299" alt="image" src="https://github.com/user-attachments/assets/9a3f61fa-0a4f-411f-b078-0c879ae29d91" />

## RESULT:
The program to demonstrate variable scope and access a static variable using both class name and object was successfully executed.


