# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
Write a program that reads two integers and divides the first by the second. Handle the case when division by zero occurs.

## AIM:
To write a Java program that performs division of two numbers and handles division-by-zero using exception handling.


## ALGORITHM :
1. Start the program.
2. Import the necessary package java.util.
3. Create a Scanner object to read input from the user.
4. Read two integers from the user.
5. Use try block to perform division.
6. Catch ArithmeticException if division by zero occurs.
7. Display appropriate output.
8. Close the scanner.
9. End the program.

## PROGRAM:
```txt
Program to implement a Exception Handling using Java
Developed by: Sudharsanam R K
RegisterNumber: 212222040163
```

## SOURCE CODE:
```java
import java.util.Scanner;

public class DivideNumbers {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int num1 = sc.nextInt();

        int num2 = sc.nextInt();

        try {
            int result = num1 / num2;
            System.out.println("Result: " + result);
        } catch (ArithmeticException e) {
            System.out.println("Error: Division by zero");
        }

        sc.close();
    }
}
```

## OUTPUT:
<img width="654" height="290" alt="image" src="https://github.com/user-attachments/assets/5a45405e-3571-4fba-b6ae-a3da0e1010db" />

## RESULT:
The program was executed successfully and exception handling was implemented to prevent division-by-zero errors.


