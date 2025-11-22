# Ex.No:2(B) METHODS

## QUESTION:
Write a class with one static method and one non-static method. Call both from the main() method.

When staticMethod() is called, it should print  "I am static".

When nonStaticMethod() is called, it should print  "I am non-static"
## AIM:
To write a Java class that contains one static method and one non-static method, and call both from the main() method.


## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class with:
    ->A static method named staticMethod() that prints "I am static".
    ->A non-static method named nonStaticMethod() that prints "I am non-static".
4.In the main() method:
    ->Call the static method directly using the class name or by its name.
    ->Create an object of the class.
    ->Call the non-static method using the object.
5.Stop the program
```

## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: Mythili D
RegisterNumber: 212222040104
*/
```

## SOURCE CODE:
```
import java.util.*;
class Go
{
    public void staticMethod()
    {
        System.out.println("I am static");
    }
    public void nonStaticMethod()
    {
        System.out.println("I am non-static");
    }
}
public class Main
{
    public static void main(String[] args)
    {
        Go obj=new Go();
        obj.staticMethod();
        obj.nonStaticMethod();
    }
}
```

## OUTPUT:

<img width="1245" height="277" alt="image" src="https://github.com/user-attachments/assets/f1c2114a-a0a6-47d9-a942-6961b01aa3f9" />


## RESULT:
The program successfully demonstrates calling a static method without an object and a non-static method using an object.
