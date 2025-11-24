# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a program to count the number of characters in a file.
## AIM:
To write a Java program that reads a file and counts the total number of characters present in it.

## ALGORITHM :
```
1. Start the program.
2. Import the necessary package 'java.util'
3. Open a text file using FileReader (e.g., "sample.txt").
4. Initialize a counter variable to zero.
5. Read characters one by one using read() method.
6. For each character read, increment the counter.
7. Stop when read() returns -1 (end of file).
8. Display the total count of characters.
9. Close the file and end the program.

```



## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: Agalya R
RegisterNumber: 212222040003
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String text = sc.nextLine();

        try {
            FileWriter fw = new FileWriter("data.txt");
            fw.write(text);
            fw.close();

            int count = text.length();
            System.out.println("Number of characters written to the file: " + count);

        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```





## OUTPUT:



<img width="1220" height="394" alt="image" src="https://github.com/user-attachments/assets/fc76d486-e727-463f-aa31-17df7eab24d4" />


## RESULT:
The program successfully reads a text file using FileReader and counts the number of characters by reading each character one by one until the end of the file.


