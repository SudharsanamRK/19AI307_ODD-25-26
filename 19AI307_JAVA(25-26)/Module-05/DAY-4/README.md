# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for determine the priority and name of the current thread.

Note : Read the threadname from the User

For example:
| Input | Result |
|--------|--------|
| NewThread | Priority of Thread: 5 <br> Name of Thread: NewThread <br> Thread[NewThread,5,Main]|

## AIM:
To write a Java program that reads a thread name from the user, sets the current thread’s name, and displays its priority and full thread details.

## ALGORITHM :
1. Start the program and import the necessary utilities.
2. Read a thread name from the user using a Scanner.
3. Retrieve the current thread using Thread.currentThread().
4. Set the name of the current thread using setName().
5. Obtain the thread’s priority using getPriority().
6. Display the thread’s name, priority, and full thread information.
7. End the program.

## PROGRAM:
```txt
Program to implement a Thread Priority Concept using Java
Developed by: Sudharsanam R K
RegisterNumber:212222040163
```

## SOURCE CODE:
```java
import java.util.Scanner;

public class CurrentThreadDetails {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String threadName = sc.nextLine();

        Thread t = Thread.currentThread();
        t.setName(threadName);

        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());
        System.out.println(t);
    }
}
```

## OUTPUT:
<img width="864" height="243" alt="image" src="https://github.com/user-attachments/assets/0ba69fad-41f4-4606-aafe-daaa8a52646f" />

## RESULT:
The program successfully reads a custom name for the current thread, assigns it to the running thread, and displays the thread’s priority and complete thread details.
