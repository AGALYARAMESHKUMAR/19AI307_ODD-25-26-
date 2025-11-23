# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Create a base class BankAccount with methods deposit() and withdraw().

1.Create two subclasses:

  ->SavingsAccount: allows withdrawal but limits it to ₹10,000 per transaction.

  ->CheckingAccount: allows withdrawal with a ₹10 fee per transaction.

2.Input account type, deposit amount, and withdrawal amount from the user.

3.If checking account has insufficient balance print - "Insufficient balance in CheckingAccount (including ₹10 fee)."

## AIM:
To develop a Java program using inheritance that simulates bank account operations with deposit and withdraw functions.

## ALGORITHM :
```
1.Start the program.
2.Import the necessary package 'java.util'
3.Create a base class BankAccount with:
   ->Variable: balance
   ->Methods: deposit(), withdraw()
4.Create subclass SavingsAccount:
   ->Override withdraw() to check limit: max ₹10,000.
5.Create subclass CheckingAccount:
   ->Override withdraw() to deduct additional ₹10 withdrawal fee.
6.If balance insufficient (amount + 10 fee), print message.
7.Read from user:
   ->Account Type (Savings/Checking)
   ->Deposit Amount
   ->Withdrawal Amount
8.Perform deposit and withdrawal.
9.Display balance or error message.
10.End the program.


```

## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: Mythili D
RegisterNumber:  212222040104
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class BankAccount {
    protected double balance;

    public void deposit(double amount) {
        balance += amount;
        System.out.println("Deposited: ₹" + amount);
    }

    public void withdraw(double amount) {
        if (amount <= balance) {
            balance -= amount;
            System.out.println("Withdrawn: ₹" + amount);
        } else {
            System.out.println("Insufficient balance.");
        }
    }
}

class SavingsAccount extends BankAccount {

    @Override
    public void withdraw(double amount) {
        if (amount > 10000) {
            System.out.println("Withdrawal limit for SavingsAccount is ₹10,000 per transaction.");
        } else if (amount <= balance) {
            balance -= amount;
            System.out.println("Withdrawn from SavingsAccount: ₹" + amount);
        } else {
            System.out.println("Insufficient balance in SavingsAccount.");
        }
    }
}

class CheckingAccount extends BankAccount {

    @Override
    public void withdraw(double amount) {
        double total = amount + 10;  // ₹10 fee

        if (total <= balance) {
            balance -= total;
            System.out.println("Withdrawn from CheckingAccount: ₹" + amount + " (₹10 fee applied)");
        } else {
            System.out.println("Insufficient balance in CheckingAccount (including ₹10 fee).");
        }
    }
}

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String type = sc.nextLine();
        double depositAmt = sc.nextDouble();
        double withdrawAmt = sc.nextDouble();

        BankAccount account;

        if (type.equalsIgnoreCase("savings")) {
            account = new SavingsAccount();
        } else {
            account = new CheckingAccount();
        }

        account.deposit(depositAmt);
        account.withdraw(withdrawAmt);

        System.out.printf("Final Balance: ₹%.2f\n", account.balance);

        sc.close();
    }
}
```






## OUTPUT:
<img width="1305" height="421" alt="image" src="https://github.com/user-attachments/assets/837123d4-76a8-40d5-b9f9-77897e428f52" />



## RESULT:
The program successfully demonstrates inheritance by performing deposit and withdrawal operations for Savings and Checking accounts
