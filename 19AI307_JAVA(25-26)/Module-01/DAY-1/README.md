# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:

A shop keeper would like to welcome their customers with their name.

Write a java program to get name from the user (String) and print it.

**Input Format:**

A single line string input.

**Output Format:**

Hello, [name]

**Example Input:** Ajeesh 

**Result :** Hello, Ajeesh

## AIM:
To write a Java program that gets the user's name as input (String) and prints a welcome message.

## ALGORITHM :
1. Start the program.
2. Import the necessary package 'java.util'
3. Create a Scanner object to read input from the user.
4. Read a string input (the user's name).
5. Store the input in the variable name.
6. Display the message: "Hello, " + name

## PROGRAM:
```txt
Program to implement variables and Operators using Java
Developed by: Sudharsanam R K
RegisterNumber:  212222040163
```

## SOURCE CODE
```java
import java.util.*;
public class prog{
    public static void main(String[] args){
        Scanner sc= new Scanner(System.in);
        String name = sc.next();
        System.out.print("Hello, "+name);
    }
}
```

## OUTPUT:
<img width="557" height="200" alt="image" src="https://github.com/user-attachments/assets/98db669e-de66-4c23-b76d-49b6a9a6754f" />

## RESULT:
Thus, the java program to get name from the user (String) and print it is executed successfully.
