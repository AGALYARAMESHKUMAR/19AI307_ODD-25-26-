# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
If an Integer object is set to null, and you attempt to call .toString() on it, what happens? How can you prevent your code from throwing an exception in such cases?

## AIM:
To write a Java program that demonstrates what happens when calling .toString() on a null Integer object and how to prevent the program from throwing a NullPointerException.

## ALGORITHM :
```
1.Start the program.
2.Import the necessary package 'java.util'
3.Declare an Integer object and assign it as null.
4.Try to print the value using .toString().
5.Check if the object is null before calling .toString().
6.If not null, call .toString(); otherwise print a safe message or use String.valueOf() to avoid an exception.
7.Display the output.
8.End the program.
```




## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Mythili D
RegisterNumber: 212222040104 
*/
```

## SOURCE CODE:

```
import java.util.*;
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        
        try
        {
            Integer s=sc.nextInt();
            if(s==null || s==0){
                throw new NullPointerException();
            }
            else{
                System.out.println(s.toString());
            }
        }
        catch(Exception e)
        {
            System.out.println("Null Integer");
        }
    }
}
```





## OUTPUT:
<img width="1321" height="421" alt="image" src="https://github.com/user-attachments/assets/9adb4edd-f2ae-4cc8-a6f6-bf80dc84eb75" />



## RESULT:
The program successfully prevents a NullPointerException by validating the object before calling .toString() and using safe wrapper methods to display null values.
