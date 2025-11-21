# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Maintain two int variables a and b, read their initial values from user. Use synchronized block to swap them and print swapped values.

**Input:**
- Two lines: a and b values

**Output:**
- a = <swapped_a>
- b = <swapped_b>

For example:

| Input | Result |
|--------|--------|
| 5 <br> 10| a = 10 <br> b = 5 |


## AIM:
To write a Java program that demonstrates the use of the synchronized block by swapping two numbers safely using a lock object.

## ALGORITHM :
1. Start the program and import the required utility package.
2. Read two integer values from the user.
3. Create a lock object to control synchronization.
4. Use a synchronized block with the lock object.
5. Inside the synchronized block, swap the values of the two variables using a temporary variable.
6. After swapping, display the updated values of both variables.
7. End the program.	

## PROGRAM:
```txt
Program to implement a Synchronization concept using Java
Developed by: Sudharsanam R K
RegisterNumber: 212222040163
```

## SOURCE CODE:
```java
import java.util.Scanner;

public class SwapUsingSync {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();

        Object lock = new Object();

        synchronized (lock) {
            int temp = a;
            a = b;
            b = temp;
        }

        System.out.println("a = " + a);
        System.out.println("b = " + b);
    }
}
```

## OUTPUT:
<img width="439" height="374" alt="image" src="https://github.com/user-attachments/assets/f51f5de3-82d5-4a91-bca3-65bc1fdc1a28" />

## RESULT:
The program successfully demonstrates synchronization by swapping two numbers within a synchronized block, ensuring thread-safe execution even though only one thread is used.
