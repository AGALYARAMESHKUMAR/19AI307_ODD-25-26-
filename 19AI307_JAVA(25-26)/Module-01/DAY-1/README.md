# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely is training to become a logic wizard. She enters a gate that tests her understanding of logical conditions.

She is given two magical conditions:

hasKey – whether she has the golden key (boolean)

knowsPassword – whether she knows the secret password (boolean)

The gate then evaluates her truthfulness using logical operators:

<img width="390" height="134" alt="m1(a)" src="https://github.com/user-attachments/assets/72c8eec9-b802-4240-9ca9-484cd3320b14" />


Write a program that:

Accepts two boolean inputs: hasKey and knowsPassword

Displays the results of:

hasKey && knowsPassword
hasKey || knowsPassword
!hasKey
!knowsPassword
**Input Format:**

First line: true or false (hasKey)

Second line: true or false (knowsPassword)

**Output Format:**

Access with AND: <true/false>

Access with OR: <true/false>

Does NOT have key: <true/false>

Does NOT know password: <true/false>

## AIM:
To write a Java program that reads two integer numbers from the user and performs basic arithmetic operations such as addition, subtraction, multiplication, division, and modulus, and displays the results.


## ALGORITHM :
1. Start
2. Create a Scanner object to read input from the user.
3. Read two boolean values i and j from the user.
4. Compute the following:
       l1 = i && j → Logical AND of i and j
   
       l2 = i || j → Logical OR of i and j
   
       l3 = !i → Logical NOT of i
   
       l4 = !j → Logical NOT of j
   
5.Display the results:

      "Access with AND: " + l1

      "Access with OR: " + l2

       "Does NOT have key: " + l3

      "Does NOT know password: " + l4

6. Stop

## PROGRAM:
 ```

Program to implement variables and Operators using Java
Developed by: ARINI A
RegisterNumber:  212222040011

```

## Sourcecode.java:
```
import java.util.*;
public class Main{
    public static void main(String[]args)
    {
        Scanner sc=new Scanner(System.in);
        boolean i=sc.nextBoolean();
        boolean j = sc.nextBoolean();
        boolean l1=(i&&j);
        boolean l2=(i||j);
        boolean l3=(!i);
        boolean l4=(!j);
        System.out.println("Access with AND: "+l1);
        System.out.println("Access with OR: "+l2);
        System.out.println("Does NOT have key: "+l3);
        System.out.println("Does NOT know password: "+l4);
    }
}
```
## OUTPUT:
<img width="848" height="415" alt="m1(b)" src="https://github.com/user-attachments/assets/abeb199c-284f-42d9-ab45-9c5707adb51f" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.











