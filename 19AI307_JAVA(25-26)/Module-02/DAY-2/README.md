# Ex.No:2(B) METHODS

## QUESTION:
Create a method printName(String name) that gets input from the user for the string and prints "Hello, " followed by the name passed.

## AIM:
To write a Java program to implement methods in Java by passing a string as a parameter to a method and printing a greeting message

## ALGORITHM :
1. Start the program.
2. Import the necessary package java.util.
3. Define a class prog.
4. Declare a method printName(String name) that prints "Hello, " followed by the name.
5. In the main() method, get input from the user using Scanner.
6. Create an object of the class.
7. Call the method and pass the input as an argument.
8. End the program.


## PROGRAM:
```
Program to implement a Methods using Java
Developed by: Sudharsanam R K
RegisterNumber: 212222040163
```

## SOURCE CODE:
```java
import java.util.*;

class prog{
    String name;
    void printName(){
        Scanner sc=new Scanner(System.in);
        String str=sc.nextLine();
        System.out.println("Hello, "+str);
    }
    public static void main(String[] args){
        prog obj=new prog();
        obj.printName();
    }
}
```

## OUTPUT:
<img width="371" height="155" alt="image" src="https://github.com/user-attachments/assets/50045644-bf22-4d45-b1fa-ee7ef6b7e71f" />

## RESULT:
The program to implement methods in Java was successfully executed and displayed a greeting message using a parameterized method.
