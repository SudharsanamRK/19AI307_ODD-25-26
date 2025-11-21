# Ex.No:5(C)  FILE HANDLING USING JAVA

## QUESTION:
Write a Java program to create a new file named example.txt.

For example:

| Result |
|--------|
| File created: example.txt |

## AIM:
To write a Java program that demonstrates basic file handling by creating a new file using the File class and the createNewFile() method.

## ALGORITHM :
1. Start the program and import the required java.io.File package.
2. Create a File object and specify the filename to be created.
3. Call the createNewFile() method to attempt file creation.
4. Check if the file is successfully created.
5. If created, display the file name to the user.
6. Handle any exceptions that may occur during file creation.
7. End the program.	

## PROGRAM:
```txt
Program to implement a File Handling using Java
Developed by: Sudharsanam R K
RegisterNumber: 212222040163
```

## SOURCE CODE:
```java
import java.io.File;

public class CreateFileExample {
    public static void main(String[] args) {
        try {
            File file = new File("example.txt");
            if (file.createNewFile()) {
                System.out.println("File created: " + file.getName());
            }
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```
## OUTPUT:
<img width="745" height="199" alt="image" src="https://github.com/user-attachments/assets/f433c867-19d7-4f18-92a5-40477cbecd2d" />

## RESULT:
The program successfully creates a new file named example.txt in the project directory. If the file already exists, the program simply terminates without creating a duplicate.
