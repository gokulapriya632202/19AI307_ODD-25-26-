# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A fuel station sells two types of fuels: Petrol and Diesel.
There is a base class named Fuel, which has the following attributes: fuelId (a string representing the fuel transaction ID), customerName (the name of the customer), litersPurchased (the quantity of fuel bought in liters), and pricePerLiter (the cost of one liter of the fuel).
Two classes, Petrol and Diesel, inherit from the Fuel class. The Petrol class applies a 3% discount on the total bill amount, whereas the Diesel class applies a 5% discount on the total bill amount.
Your task is to write a program that accepts exactly three fuel purchase records. Each record starts with the fuel type (either Petrol or Diesel), followed by the fuelId, customerName, litersPurchased, and pricePerLiter.
For each record, the program should calculate the total price after applying the respective discount and display the details of the purchase, including the discount rate and the final amount payable.

## AIM:
To create a program that reads three fuel purchase records (Petrol or Diesel), calculates the total bill for each based on liters and price per liter, applies the respective discount (3% for Petrol, 5% for Diesel), and displays the complete purchase details with the final payable amount.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a base class Fuel with attributes and methods to calculate price and get discount rate.
4.	Create subclasses Petrol and Diesel that override the discount rate (3% for Petrol, 5% for Diesel).
5.	Based on the input fuel type, create the corresponding object (Petrol, Diesel, or Fuel).
6.	Calculate the total amount by multiplying litersPurchased and pricePerLiter.
7.	Apply the discount using the overridden getDiscountRate() method.
8.	Display all purchase details including discount rate and final payable amount, then end the program.

## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: GOKULA PRIYA P
RegisterNumber: 212222040044
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
import java.text.DecimalFormat;

class Fuel {
    String fuelId, customerName;
    double litersPurchased, pricePerLiter;

    Fuel(String fuelId, String customerName, double litersPurchased, double pricePerLiter) {
        this.fuelId = fuelId;
        this.customerName = customerName;
        this.litersPurchased = litersPurchased;
        this.pricePerLiter = pricePerLiter;
    }

    int getDiscountRate() {
        return 0;
    }

    double calculateTotalPrice() {
        double total = litersPurchased * pricePerLiter;
        double discountAmount = total * getDiscountRate() / 100.0;
        return total - discountAmount;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Fuel ID: " + fuelId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("Fuel Type: General");
        System.out.println("Liters Purchased: " + litersPurchased);
        System.out.println("Price per Liter: " + pricePerLiter);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Total Price: " + df.format(calculateTotalPrice()));
    }
}

class Petrol extends Fuel {
    Petrol(String fuelId, String customerName, double litersPurchased, double pricePerLiter) {
        super(fuelId, customerName, litersPurchased, pricePerLiter);
    }

    int getDiscountRate() {
        return 3;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Fuel ID: " + fuelId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("Fuel Type: Petrol");
        System.out.println("Liters Purchased: " + litersPurchased);
        System.out.println("Price per Liter: " + pricePerLiter);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Total Price: " + df.format(calculateTotalPrice()));
    }
}

class Diesel extends Fuel {
    Diesel(String fuelId, String customerName, double litersPurchased, double pricePerLiter) {
        super(fuelId, customerName, litersPurchased, pricePerLiter);
    }

    int getDiscountRate() {
        return 5;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Fuel ID: " + fuelId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("Fuel Type: Diesel");
        System.out.println("Liters Purchased: " + litersPurchased);
        System.out.println("Price per Liter: " + pricePerLiter);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Total Price: " + df.format(calculateTotalPrice()));
    }
}

public class FuelStation {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String type = sc.next();
        String id = sc.next();
        String name = sc.next();
        double liters = sc.nextDouble();
        double rate = sc.nextDouble();

        Fuel fuel;
        if (type.equalsIgnoreCase("Petrol")) {
            fuel = new Petrol(id, name, liters, rate);
        } else if (type.equalsIgnoreCase("Diesel")) {
            fuel = new Diesel(id, name, liters, rate);
        } else {
            fuel = new Fuel(id, name, liters, rate);
        }

        fuel.display();
        sc.close();
    }
}
```
## OUTPUT:
<img width="941" height="737" alt="image" src="https://github.com/user-attachments/assets/43018dc6-09e9-4bce-a66c-bca4ffa5615b" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.

