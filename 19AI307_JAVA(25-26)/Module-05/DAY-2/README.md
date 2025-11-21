# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.

| Input | Result |
|-------|--------|
| 2 <br>101 <br>Alice <br>89.5 <br>102 <br>Bob <br>92.0 | Students serialized successfully into: students.dat <br>Students deserialized successfully from: students.dat <br><br>Deserialized Students:<br>Student{id=101, name='Alice', marks=89.5}<br>Student{id=102, name='Bob', marks=92.0} |

## AIM:
To write a Java program that demonstrates object serialization and deserialization, where multiple Student objects entered by the user are stored in a file and later retrieved and displayed.

## ALGORITHM :
1. Start the program and import required I/O and utility packages.
2. Create a Student class that implements Serializable.
3. Read the number of students and their details from the user and store them in a list.
4. Open an ObjectOutputStream and write the list of Student objects to a file.
5. Open an ObjectInputStream and read back the list of Student objects from the file.
6. Display the deserialized student details on the screen.
7. Handle all I/O exceptions that occur during serialization and deserialization.

## PROGRAM:
```txt
Program to implement a Serialization and Deserialization using Java
Developed by: Sudharsanam R K 
RegisterNumber: 212222040163
```

## SOURCE CODE:
```java
import java.io.*;
import java.util.*;

class Student implements Serializable {
    private static final long serialVersionUID = 1L;
    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput {

    public static void serializeStudents(List<Student> students, String fileName) {
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);
        } catch (IOException e) {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }

    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName) {
        List<Student> students = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName))) {
            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        return students;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = scanner.nextInt();
        scanner.nextLine();

        for (int i = 0; i < n; i++) {
            int id = scanner.nextInt();
            scanner.nextLine();
            String name = scanner.nextLine();
            double marks = scanner.nextDouble();
            scanner.nextLine();
            students.add(new Student(id, name, marks));
        }

        String fileName = "students.dat";

        serializeStudents(students, fileName);

        List<Student> deserializedStudents = deserializeStudents(fileName);

        if (deserializedStudents != null) {
            System.out.println("\nDeserialized Students:");
            for (Student s : deserializedStudents) {
                System.out.println(s);
            }
        }
        scanner.close();
    }
}
```

## OUTPUT:
<img width="1185" height="438" alt="image" src="https://github.com/user-attachments/assets/ca8be353-e951-4f83-885d-b67afe668ae1" />

## RESULT:
The program successfully serializes a list of Student objects into a file named students.dat and then deserializes the data back into a list. It correctly displays all the retrieved student information, proving that object serialization and deserialization work as expected.
