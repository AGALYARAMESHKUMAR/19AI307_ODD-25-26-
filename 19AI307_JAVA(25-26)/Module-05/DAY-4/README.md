# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for set the priority and name of the current thread.Consider two threads t1 and t2

Note : Read the threadname from the User

set the priority as 4 for t1 and set the priority as 2 for t2


## AIM:
To write a Java program to set and display the name and priority of two threads (t1 and t2).
The thread names must be read from the user.


## ALGORITHM :
```
1.Start the program.
2.Import the necessary package 'java.util'
3.Create a class MyThread that extends Thread.
4.In the main method:
   ->Create Scanner object.
   ->Read two thread names from the user.
   ->Create two thread objects t1 and t2.
   ->Set names to the threads.
5.Set priorities: t1 → 4 and t2 → 2.
6.Start both threads.
7.Display thread name and priority inside run() method.
8.Stop the program.
```




## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: Mythili D
RegisterNumber: 212222040104 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class ThreadPriorityExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String name1 = scanner.nextLine();
        String name2 = scanner.nextLine();
        Thread t1 = new Thread();
        Thread t2 = new Thread();
        t1.setName(name1);
        t2.setName(name2);
        t1.setPriority(4);
        t2.setPriority(2);
        System.out.println(t1);
        System.out.println(t2);

        scanner.close();
    }
}
```






## OUTPUT:
<img width="1296" height="391" alt="image" src="https://github.com/user-attachments/assets/54f8521a-0274-4065-b9a0-80900bb8b7c1" />



## RESULT:

The program successfully reads thread names from the user, assigns different priorities (4 and 2) to two threads and prints their names along with their priority when executed.
