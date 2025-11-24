# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:

finalPrice = purchaseWeight * (goldRatePerGram - discount)

For PremiumCustomer, additionally show cashback amount (which is 1% of the final price).

## AIM:

To write a Java program using inheritance to calculate the final gold price for Regular and Premium customers based on discounts.
## ALGORITHM :
```
1.Start the program.
2.Import the necessary package 'java.util'
3.Create a base class Customer with attributes:
   ->customerId, name, purchaseWeight.
4.Create RegularCustomer that:
   ->Gets 2% discount on gold price per gram.
5.Create PremiumCustomer that:
   ->Gets 5% discount on gold price per gram.
   ->Gets 1% cashback on final billed amount.
6.Input Gold rate per gram from the user.
7.For each customer:
   ->Calculate discountAmount = goldRatePerGram * discountPercentage
   ->Calculate finalPrice = purchaseWeight * (goldRatePerGram - discountAmount)
8.For Premium customer:
   ->Calculate cashback = 1% of finalPrice
9.Display final results.
10.End the program.
```



## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: Agalya R
RegisterNumber: 212222040003
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
import java.text.DecimalFormat;

class Customer {
    String customerId, name;
    double purchaseWeight, goldRatePerGram;

    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }

    double getDiscountRate() {
        return 0;
    }

    double calculateFinalPrice() {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100;
        double effectiveRate = goldRatePerGram - discountAmount;
        return purchaseWeight * effectiveRate;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: General");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class RegularCustomer extends Customer {
    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    double getDiscountRate() {
        return 2;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Regular");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class PremiumCustomer extends Customer {
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    double getDiscountRate() {
        return 5;
    }

    double getCashback() {
        return 0.01 * calculateFinalPrice();
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Premium");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
        System.out.println("Cashback: " + df.format(getCashback()));
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String customerType = sc.nextLine().trim();
        String id = sc.nextLine().trim();
        String name = sc.nextLine().trim();
        double weight = sc.nextDouble();
        double rate = sc.nextDouble();

        Customer customer;

        if (customerType.equalsIgnoreCase("Regular")) {
            customer = new RegularCustomer(id, name, weight, rate);
        } else if (customerType.equalsIgnoreCase("Premium")) {
            customer = new PremiumCustomer(id, name, weight, rate);
        } else {
            customer = new Customer(id, name, weight, rate);
        }

        customer.display();
    }
}
```






## OUTPUT:

<img width="1286" height="718" alt="image" src="https://github.com/user-attachments/assets/916a9af7-9871-4535-95b9-b39bfe32350a" />


## RESULT:
The program successfully calculates the final gold price using inheritance and executed successfully.


