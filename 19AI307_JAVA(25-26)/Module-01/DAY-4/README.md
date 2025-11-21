# Ex.No:1(D) ARRAYS

## QUESTION:

Write a Java program to sort an array in ascending order.

Example Input:

5

5

3

8

6

2

Result:
2 3 5 6 8

## AIM:
To write a Java program that reads an array of integers and sorts the elements in ascending order using built-in array methods.

## ALGORITHM :
1.  Start the program.
2.  Import the required package java.util.
3.  Read the size of the array from the user.
4.  Declare an integer array with the given size.
5.  Read each array element using a loop.
6.  Use Arrays.sort() to sort the array in ascending order.
7.  Print the sorted array elements.
8.  End the program.

## PROGRAM:
```txt
Program to implement an Array concept using Java
Developed by: Sudharsanam R K
RegisterNumber: 212222040163
```

## SOURCE CODE:
```java
import java.util.*;
public class Main {
    public static void main(String[]args) {
        Scanner sc = new Scanner(System.in);
        int size = sc.nextInt();
        int[] arr = new int[size];
        
        for (int i = 0; i < size; i++) 
            arr[i] = sc.nextInt();
        
        Arrays.sort(arr);
        
        for (int i = 0; i < size; i++)
            System.out.print(arr[i] + " ");
    }
}
```

## OUTPUT:
<img width="371" height="532" alt="image" src="https://github.com/user-attachments/assets/9e10ecac-6ff9-47de-aa00-55c12d392012" />

## RESULT:
Thus, the Java program to sort an array in ascending order was executed successfully.
