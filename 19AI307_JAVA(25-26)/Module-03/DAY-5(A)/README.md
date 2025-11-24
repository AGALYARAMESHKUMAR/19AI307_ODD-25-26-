# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to define an enum named Department with constants like CS, IT, and ECE. Each constant should hold a full form string like "Computer Science" using a constructor.


## AIM:
To write a Java program that defines an enum named Department with constants CS, IT, and ECE, where each constant stores its full-form name using a constructor.

## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an enum named Department.
4.Add constants: CS, IT, ECE.
5.Assign each constant a full-form string using a parameterized constructor inside the enum.
6.Store the full-form string in a variable.
7.Provide a getter method to return the string.
8.Display the full form of each department using values().
9.End the program.
```




## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: Agalya R
RegisterNumber: 212222040003
*/
```

## SOURCE CODE:
```
import java.util.*;

enum Department {
    CS("Computer Science"),
    IT("Information Technology"),
    ECE("Electronics and Communication Engineering");

    private String fullForm;

    Department(String fullForm) {
        this.fullForm = fullForm;
    }

    public String getFullForm() {
        return fullForm;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String dep = sc.next().toUpperCase();

        try {
            Department d = Department.valueOf(dep);
            System.out.println("Full Form: " + d.getFullForm());
        } catch (Exception e) {
            System.out.println("Invalid department code entered.");
        }
    }
}
```






## OUTPUT:
<img width="1257" height="412" alt="image" src="https://github.com/user-attachments/assets/7098e4f6-bb65-4aef-b135-7fe3f2e1b116" />



## RESULT:

The program successfully defines an enum Department with constants that store their full-form names using a constructor and displays their values.

