# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:

Write a Java program to create a class called BankAccount with private instance variables accountNumber and balance. Provide public getter and setter methods to access and modify these variables.


## AIM:
To write a Java program to create a class BankAccount with private instance variables accountNumber and balance, and provide public getter and setter methods to access and modify them.

## ALGORITHM :
```
1.Start the program.
2.Import the necessary package 'java.util'
3.Create a class named BankAccount.
4.Declare two private instance variables:
  ->accountNumber (String or long)
  ->balance (double)
5.Create public setter methods to set values of accountNumber and balance.
6.Create public getter methods to retrieve values of accountNumber and balance.
7.In the main() method:
   ->Create an object of BankAccount.
   ->Use setter methods to assign values.
   ->Use getter methods to display the values.
11.Stop the program.
```


## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: Agalya R
RegisterNumber: 212222040003
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class BankAccount {
    private String accountNumber;
    private double balance;

    public String getAccountNumber() {
        return accountNumber;
    }
    public void setAccountNumber(String accountNumber) {
        this.accountNumber = accountNumber;
    }

    public double getBalance() {
        return balance;
    }
    public void setBalance(double balance) {
        this.balance = balance;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        BankAccount account = new BankAccount();

        // Input account number and balance
        account.setAccountNumber(scanner.nextLine());
        account.setBalance(scanner.nextDouble());

        // Print details
        System.out.println("Account Number: " + account.getAccountNumber());
        System.out.println("Balance: " + account.getBalance());

        scanner.close();
    }
}
```

## OUTPUT:

<img width="1235" height="468" alt="image" src="https://github.com/user-attachments/assets/5afa2ab5-3010-46e8-831a-d49f1551d662" />



## RESULT:
The program successfully demonstrates how to use private variables with public getter and setter methods to protect and access data in a class.

