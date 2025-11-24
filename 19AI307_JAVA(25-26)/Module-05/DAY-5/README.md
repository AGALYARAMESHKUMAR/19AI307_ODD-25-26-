# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Print "Hello" and "World" alternately from two threads using synchronized blocks.

## AIM:
To write a Java program that creates two threads that print “Hello” and “World” alternately.
The two threads must coordinate using synchronized blocks with wait() and notify().

## ALGORITHM :
```
1. Start the program.
2. Import the necessary package 'java.util'
3. Create a class PrintMessage with a shared boolean variable helloTurn to control switching.
4. Create two synchronized methods:
   a) printHello() → prints “Hello” when it's its turn; otherwise waits.
   b) printWorld() → prints “World” when it's its turn; otherwise waits.
5. In each method:
   a) Use while() loop to check whose turn it is.
   b) Use wait() to block if not its turn.
6. Print the message, change the turn flag, and call notify() to wake the other thread.
7. Create a main class and start two threads, one calling printHello() and the other calling printWorld().
8. End the program.
```




## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: Agalya R
RegisterNumber: 212222040003
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class PrintAlternately {
    private final int n;
    private boolean helloTurn = true; 
    private final Object lock = new Object();

    public PrintAlternately(int n) {
        this.n = n;
    }

    public void printHello() {
        for (int i = 0; i < n; i++) {
            synchronized (lock) {
                while (!helloTurn) {
                    try {
                        lock.wait();
                    } catch (InterruptedException e) {
                        Thread.currentThread().interrupt();
                    }
                }
                System.out.println("Hello");
                helloTurn = false;
                lock.notify();
            }
        }
    }

    public void printWorld() {
        for (int i = 0; i < n; i++) {
            synchronized (lock) {
                while (helloTurn) {
                    try {
                        lock.wait();
                    } catch (InterruptedException e) {
                        Thread.currentThread().interrupt();
                    }
                }
                System.out.println("World");
                helloTurn = true;
                lock.notify();
            }
        }
    }
}
public class HelloWorldAlternately {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt(); 
        scanner.close();

        PrintAlternately printer = new PrintAlternately(n);

        Thread t1 = new Thread(() -> printer.printHello());
        Thread t2 = new Thread(() -> printer.printWorld());

        t1.start();
        t2.start();

        try {
            t1.join();
            t2.join();
        } catch (InterruptedException e) {
            Thread.currentThread().interrupt();
        }
    }
}
```






## OUTPUT:
<img width="1224" height="724" alt="image" src="https://github.com/user-attachments/assets/ef675f04-6568-4925-b97f-0547227551d1" />



## RESULT:
The program successfully prints “Hello” and “World” alternately using two separate threads. Synchronization using wait() and notify() ensures that the two threads print in a coordinated manner without overlapping.

