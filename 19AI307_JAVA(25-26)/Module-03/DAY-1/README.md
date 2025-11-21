# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
Create a Super class Person with fields name and age. Create a subclass Student that inherits from Person and adds a field marks (integer). Implement a method in Student called calculateGrade() which returns the grade based on the marks:
- Marks ≥ 90: Grade A
- Marks ≥ 75 and < 90: Grade B
- Marks ≥ 50 and < 75: Grade C
- Marks < 50: Grade F

## AIM:
To develop a Java program that demonstrates single inheritance by creating a Student class that inherits from Person, accepts user input, and displays student details along with the calculated grade based on marks.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the student's name, age, and marks from the user.
4. Create a Student object by passing the input values to its constructor.
5. Invoke the displayInfo() method of the Student object.
6. Print the student's details: name, age, and marks.
7. Determine the grade using conditional statements and display it.

## PROGRAM:
```txt
Program to implement a Inheritance and Aggregation using Java
Developed by: Sudharsanam R K
RegisterNumber:212222040163
```

## SOURCE CODE:
```java
import java.util.*;
class Person {
    String name;
    int age;

    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
}
class Student extends Person {
    int marks;

    Student(String name, int age, int marks) {
        super(name, age);
        this.marks = marks;
    }
    void displayInfo() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Marks: " + marks);

        if (marks >= 90)
            System.out.println("Grade: A");
        else if (marks >= 75)
            System.out.println("Grade: B");
        else if (marks >= 50)
            System.out.println("Grade: C");
        else
            System.out.println("Grade: F");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        int age = sc.nextInt();
        int marks = sc.nextInt();

        Student s = new Student(name, age, marks);
        s.displayInfo();
    }
}
```

## OUTPUT:
<img width="578" height="697" alt="image" src="https://github.com/user-attachments/assets/31780cd3-b480-444e-a370-5c927f538d51" />

## RESULT:
The program successfully reads the student’s details, creates a Student object using inheritance, and displays the student’s information along with the appropriate grade based on the marks entered.
