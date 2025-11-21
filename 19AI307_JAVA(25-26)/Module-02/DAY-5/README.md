# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Calculator with: One non-static method add(int a, int b) that returns the sum, One static method info() that says "Calculator is ready".

| Input      | Result                     |
|------------|-----------------------------|
| 10<br>20   | Calculator is ready<br>Sum: 30 |


## AIM:
To implement access modifiers in Java using both static and non-static methods within a class.


## ALGORITHM :
1. Start the program.
2. Import the necessary package java.util.
3. Create a class Calculator.
4. Define a non-static method add(int a, int b) to compute sum.
5. Define a static method info() that prints a message.
6. In main(), get two numbers from the user.
7. Call the static method using class name.
8. Create an object and call the non-static add() method.
9. Print the sum.
10. End the program.

## PROGRAM:
```txt
Program to implement a Access Modifiers using Java
Developed by: Sudharsanam R K
RegisterNumber: 212222040163
```

## SOURCE CODE:
```java
import java.util.Scanner;

class Calculator {
    int add(int a, int b) {
        return a + b;
    }

    static void info() {
        System.out.println("Calculator is ready");
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num1 = sc.nextInt();
        int num2 = sc.nextInt();

        Calculator.info();
        Calculator calc = new Calculator();
        int sum = calc.add(num1, num2);
        System.out.println("Sum: " + sum);
    }
}
```

## OUTPUT:
<img width="546" height="308" alt="image" src="https://github.com/user-attachments/assets/60613ecc-5ed5-417a-94d7-404a84214ce8" />

## RESULT:
The program successfully implemented access modifiers using static and non-static methods in Java.



