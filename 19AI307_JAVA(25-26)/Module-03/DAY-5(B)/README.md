# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Find the largest digit in a number using wrapper class methods.

## AIM:
To write a Java program to find the largest digit in a number using wrapper class methods (such as Character.getNumericValue() and Integer.parseInt()).

## ALGORITHM :
```
1. Start the program.

2. Import the necessary package 'java.util'

3. Read a number as a String (so digits can be processed individually).

4. Initialize a variable to store the largest digit.

5. Loop through each character of the string.

6. Convert each character to a digit using a wrapper class method:
   ->Character.getNumericValue(ch)

7. Compare and update the largest digit.

8. Print the largest digit.

9. End the program.
```




## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: Agalya R
RegisterNumber: 212222040003
*/
```

## SOURCE CODE:
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();

        Integer n = num;  // Wrapper class
        int largest = 0;

        while (n > 0) {
            int digit = n % 10;
            largest = Math.max(largest, digit);
            n /= 10;
        }

        System.out.println("The largest digit is: " + largest);
    }
}
```




## OUTPUT:
<img width="1250" height="387" alt="image" src="https://github.com/user-attachments/assets/5713d801-9fac-4863-8006-9a96e8db171e" />



## RESULT:
The program successfully finds and prints the largest digit in a given number using wrapper class methods.

