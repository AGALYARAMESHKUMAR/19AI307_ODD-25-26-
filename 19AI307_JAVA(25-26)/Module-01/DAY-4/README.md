# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java Program to Find the Average of Array Elements.

## AIM:
To write a Java program that accepts elements of an array and calculates the average value of all the elements by summing them and dividing the total by the number of elements.

## ALGORITHM :
1.	Start the program.
2.	Read the number of elements and store it in a variable.
3. Read all the array elements and calculate the sum of all elements.
4. Find the average by dividing the sum by the total number of elements.
5. Display the average and stop.
   
## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: 212222040003 
RegisterNumber: Agalya R
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
public class AverageOfArray {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        
        int[] arr = new int[n];
        int sum = 0;
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
            sum += arr[i];
        }
        
        double average = (double) sum / n;
        System.out.printf("The average of elements is %.2f\n", average);
    }
}
```
## OUTPUT:
<img width="1326" height="509" alt="Screenshot 2025-11-24 212833" src="https://github.com/user-attachments/assets/4fe3242a-fdcd-4c3c-832d-5597a623c682" />


## RESULT:
The program successfully calculates and prints the average value of the elements present in the array.

