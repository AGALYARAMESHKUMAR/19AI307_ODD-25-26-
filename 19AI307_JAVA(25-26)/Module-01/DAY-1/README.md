# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
A shop keeper would like to welcome their customers with their name.

Write a java program to get name from the user (String) and print it.

Input Format:

A single line string input.

Output Format:

Hello, [name]


## AIM:
To write a Java program that reads a customer’s name as input and displays a welcome message.

## ALGORITHM :
```
1.Start the program.
2.Create a Scanner object to read input from the user.
3.Read a string input (customer name).
4.Display the message: "Hello, [name]".
5.End the program.
 ```



## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: Agalya R
RegisterNumber: 212222040003
*/
```

## Sourcecode.java:
```
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner inp = new Scanner(System.in);
        String name=inp.nextLine();
        System.out.println("Hello, "+name);
    }
}
```


## OUTPUT:
<img width="1306" height="290" alt="Screenshot (20)" src="https://github.com/user-attachments/assets/d61f7432-12d1-400a-88e0-19f5b8fd6d90" />



## RESULT:
The program successfully reads the user's name as input and prints a welcome message in the format Hello, [name].

