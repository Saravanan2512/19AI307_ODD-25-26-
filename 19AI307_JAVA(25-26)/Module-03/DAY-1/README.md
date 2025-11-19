# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:

## AIM:
To develop a Java program using inheritance to calculate the final gold purchase price for Regular and Premium customers based on purchase weight, gold rate, and applicable discounts/cashback.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a base class Customer with attributes such as customerId, name, purchaseWeight, and goldRatePerGram, and include methods for discount calculation and final price computation.
4. Create derived classes:
    RegularCustomer with a fixed 2% discount.
    PremiumCustomer with a 5% discount and an additional cashback of 1% on the final price.
5. Override methods in the derived classes to provide specific discount values and cashback functionality (for Premium customers).
6. BAccept customer details and gold rate at runtime, determine the customer type, and create the appropriate object (Regular or Premium).
7. Invoke the display method to show all details including discount, final price, and cashback (if applicable).





## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: SARAVANAN G
RegisterNumber:  212223230194
*/
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

    void display(String type) {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: " + type);
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

    @Override
    double getDiscountRate() {
        return 2;
    }

    @Override
    void display(String type) {
        super.display("Regular");
    }
}

class PremiumCustomer extends Customer {
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    @Override
    double getDiscountRate() {
        return 5;
    }

    double calculateCashback() {
        return 0.01 * calculateFinalPrice();
    }

    @Override
    void display(String type) {
        super.display("Premium");
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Cashback: " + df.format(calculateCashback()));
    }
}

public class JewelryStore {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String customerType = sc.nextLine().trim();
        String id = sc.nextLine().trim();
        String name = sc.nextLine().trim();
        double weight = Double.parseDouble(sc.nextLine().trim());
        double goldRate = Double.parseDouble(sc.nextLine().trim());

        Customer c;
        if (customerType.equalsIgnoreCase("Regular")) {
            c = new RegularCustomer(id, name, weight, goldRate);
        } else {
            c = new PremiumCustomer(id, name, weight, goldRate);
        }

        c.display(customerType);
        sc.close();
    }
}

```



## OUTPUT:

<img width="834" height="247" alt="image" src="https://github.com/user-attachments/assets/3ecfceae-9ff4-44ea-91a3-961294332d98" />


## RESULT:
Thus, the program successfully demonstrated the use of inheritance, method overriding, and runtime polymorphism to compute the final payable amount for different customer types in a jewelry store based on discounts and cashback.
