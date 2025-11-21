# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:

Write a Java program to find the longest word in a given sentence.

**Example Input:**
Apple Orange

**Result:**
The longest word is: Orange

## AIM:
To write a Java program that reads a sentence and finds the longest word using string operations.

## ALGORITHM :
1. Start the program.
2. Import the necessary package java.util.
3. Read a full sentence from the user.
4. Split the sentence into words using split(" ").
5. Initialize a variable longest to store the longest word.
6. Traverse through each word in the array:
   - Compare lengths and update longest if a longer word is found.
7. Display the longest word.
8. End the program.

## PROGRAM:
```txt
Program to implement Strings and Math Function using Java
Developed by: Sudharsanam R K
RegisterNumber: 212222040163
```

## SOURCE CODE:

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        String sentence = sc.nextLine();
        String[] words = sentence.split(" ");
        
        String longest = "";
        for (String word : words) {
            if (word.length() > longest.length()) {
                longest = word;
            }
        }
        System.out.print("The longest word is: " + longest);
        sc.close();
    }
}
```

## OUTPUT:
<img width="809" height="240" alt="image" src="https://github.com/user-attachments/assets/4db63d19-7540-4077-af69-a462f54879f6" />

## RESULT:
Thus, the Java program to find the longest word in a sentence was executed successfully.
