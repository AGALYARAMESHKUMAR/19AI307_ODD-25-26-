# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Write a Java program to reverse a number using a while loop. For example, if the input is 1234, the output should be 4321.

## AIM:
To write a Java program to reverse a given number using a while loop.

## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read an integer number from the user.
4.Initialize rev = 0.
5.Repeat using a while loop until the number becomes 0:
  ->Extract the last digit using num % 10.
  ->Multiply rev by 10 and add the digit.
  ->Divide the number by 10 (num = num / 10).
6.Print the reversed number.
7.Stop the program.
```

## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: Mythili D
RegisterNumber:  212222040104
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class ReverseNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int reversed = 0;
        while (num != 0) {
            int digit = num % 10;      
            reversed = reversed * 10 + digit; 
            num = num / 10;            
        }
        System.out.println("Reversed number: " + reversed);
        sc.close();
    }
}
```


## OUTPUT:
<img width="1263" height="375" alt="Screenshot (22)" src="https://github.com/user-attachments/assets/ecf66dba-9ed3-405e-9e19-4dccc448b268" />



## RESULT:
The program successfully reverses the given number using a while loop and displays the reversed value.
