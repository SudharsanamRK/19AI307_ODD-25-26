# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:

Write a Java program to print the Fibonacci series using a for loop. The series starts with 0 and 1, and the next number is the sum of the previous two.

**Input:** 1

**Result:** Fibonacci Series: 0 1

## AIM:

To write a Java program using a for loop to print the Fibonacci series starting from 0 and 1.

## ALGORITHM :
1. Start the program.
2. Import the necessary package java.util.
3. Create a Scanner object to read the number of terms.
4. Initialize two variables a = 0 and b = 1 to represent the first two Fibonacci numbers.
5. If the input is 1, print “0 1”.
6. Otherwise, use a for loop to generate the Fibonacci series:
   - Print the current value of a.
   - Compute the next term as next = a + b.
   - Update values: a = b and b = next.
7. End the loop and terminate the program.

## PROGRAM:

```txt
Program to implement a Looping Statement using Java
Developed by: Sudharsanam R K
RegisterNumber: 212222040163
```

## SOURCE CODE:

```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int num = input.nextInt();
        int a = 0;
        int b = 1;

        System.out.print("Fibonacci Series: ");
        
        if(num == 1) {
            System.out.print("0 1");
        } else {
            for(int i = 0; i < num; i++) {
                System.out.print(a + " ");
                int next = a + b;
                a = b;
                b = next;
            }
        }
    }
}
```

## OUTPUT:

<img width="767" height="244" alt="image" src="https://github.com/user-attachments/assets/d52c5f8d-9c8e-4890-b3dd-c8935bc096c6" />

## RESULT:
Thus, the Java program to print the Fibonacci series using a for loop was executed successfully.


