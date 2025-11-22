# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Course with attributes code, title, credits.

## AIM:
To create a Java class named Course with attributes code, title, and credits.

## ALGORITHM :
```
1.Start the program.
2.Import the necessary package 'java.util'
3.Define a class named Course.
4.Inside the class, declare three attributes:
  ->code (String)
  ->title (String)
  ->credits (int)
5.Assign values to the attributes.
6.Display the course details.
7.Stop the program.
```

## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: Mythili D
RegisterNumber: 212222040104
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Course {
    String code;
    String title;
    int credits;
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Course c1 = new Course();
        c1.code = sc.next();
        c1.title = sc.next();
        c1.credits = sc.nextInt();

        Course c2 = new Course();
        c2.code = sc.next();
        c2.title = sc.next();
        c2.credits = sc.nextInt();

        System.out.println(c1.code + " | " + c1.title + " | " + c1.credits + " credits");
        System.out.println(c2.code + " | " + c2.title + " | " + c2.credits + " credits");

        sc.close();
    }
}
```


## OUTPUT:
<img width="1230" height="341" alt="image" src="https://github.com/user-attachments/assets/1e9ecb18-3d62-414d-bb07-7ed917ef93d0" />



## RESULT:
The class Course is successfully created with attributes code, title, and credits.
