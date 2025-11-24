# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a java code to implement a class Dress with the parameterised constructor ,that accepts the cloth,cloth-type and quantity , and print the details.

## AIM:
To write a Java program to implement a class Dress with a parameterized constructor that accepts cloth, clothType, and quantity, and prints the details.

## ALGORITHM :
```
1.Start the program.
2.Import the necessary package 'java.util'
3.Create a class named Dress.
4.Declare instance variables: cloth, clothType, and quantity.
5.Create a parameterized constructor that assigns values to these variables.
6.Define a method to display the dress details.
7.In the main() method:
   ->Create an object of the Dress class using the constructor and pass values.
   ->Call the display method to print details.
8.Stop the program.
```

## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: Agalya R
RegisterNumber: 212222040003
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Dress {
    String cloth;
    String clothType;
    int quantity;

    Dress(String cloth, String clothType, int quantity) {
        this.cloth = cloth;
        this.clothType = clothType;
        this.quantity = quantity;
    }

    void display() {
        System.out.println("Dress Details:");
        System.out.println("Cloth: " + cloth);
        System.out.println("Cloth Type: " + clothType);
        System.out.println("Quantity: " + quantity);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String cloth = sc.nextLine();
        String clothType = sc.nextLine();
        int quantity = sc.nextInt();

        Dress dress = new Dress(cloth, clothType, quantity);
        dress.display();
    }
}
```


## OUTPUT:

<img width="1225" height="517" alt="image" src="https://github.com/user-attachments/assets/4dfa5c26-ff8a-45cc-bb04-254dfba5d211" />



## RESULT:
The program successfully demonstrates the use of a parameterized constructor to initialize and display dress details.

