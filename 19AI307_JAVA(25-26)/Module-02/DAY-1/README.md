# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Define a class Car with brand (String), color (String), and year (int). Create 2 different objects of Car  Assign values to attributes. Print the details of both cars.import java.util.Scanner;
## AIM:
To define a class Car with attributes brand, color, and year; create two objects of the class; assign values to their attributes; and print the details of both cars.

## ALGORITHM :
1. Define a class Car with three data members:

     String brand
     String color
     int year
 and a method printDetails() to display these values.
2. Define a class named Car with three attributes: brand, color, and year.
3. Create two objects of the Car class.
4. Assign values to the attributes of the first Car object.
5. Assign values to the attributes of the second Car object.
6. 6. Call printDetails() for car1 to display its information.
7. Call printDetails() for car2 to display its information.
8. Close the scanner and end the program.


## PROGRAM:
 ```

Program to implement a Class and Objects using Java
Developed by: Agalya R
RegisterNumber:  212222040003

```

## SOURCE CODE:
```
import java.util.Scanner;

class Car {
    String brand;
    String color;
    int year;

    void printDetails() {
        System.out.println("Brand: " + brand);
        System.out.println("Color: " + color);
        System.out.println("Year: " + year);
    }
}

class prog {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        
        Car car1 = new Car();
        car1.brand = scanner.nextLine();
        car1.color = scanner.nextLine();
        car1.year = scanner.nextInt();
        scanner.nextLine();

        
        Car car2 = new Car();
        car2.brand = scanner.nextLine();
        car2.color = scanner.nextLine();
        car2.year = scanner.nextInt();

        car1.printDetails();
        car2.printDetails();

        scanner.close();
    }
}
```


## OUTPUT:
<img width="597" height="685" alt="image" src="https://github.com/user-attachments/assets/05ebe553-f279-4f17-b125-675b4afd47bd" />


## RESULT:
The program has been executed successfully and the desired output has been obtained.




