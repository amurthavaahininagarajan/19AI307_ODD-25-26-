# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:

A food delivery application manages and processes food orders made by two categories of users: NormalUser and PrimeUser. Each food order contains basic information such as an order ID, the customer's name, the cost of the ordered items (referred to as the total amount), and the delivery charge applied to that order.

You are required to implement this system using the concept of inheritance in object-oriented programming.

The base class is called Order. It includes the following attributes:

orderId – a string representing the unique identifier for the order

customerName – a string containing the name of the person who placed the order

totalAmount – a double value representing the total cost of the food items

deliveryCharge – a double value representing the delivery fee applied to the order

From the Order class, two derived classes are created:

NormalUser:
This class represents customers who do not have any delivery benefits. For NormalUser, the final amount they need to pay is the total food cost plus the full delivery charge. The formula is:
finalAmount = totalAmount + deliveryCharge

PrimeUser:
Prime users receive a 50% discount on the delivery charge. Their final payable amount is calculated as:
finalAmount = totalAmount + (deliveryCharge × 0.5)

Your task is to develop a program that:

Accepts exactly three food order inputs from the user.

Each input begins with the user type, either "Normal" or "Prime", followed by order ID, customer name, total food amount, and delivery charge.

Depending on the user type, the final amount is calculated using the appropriate formula.

For each order, the program should display the full details including the user type and final payable amount.
 

## AIM:

To calculate and display the final order amount for Normal and Prime users using inheritance and method overriding.
## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an Order class with order details and a method to calculate the final amount.
4.Create NormalUser and PrimeUser classes that inherit from Order.
5.Override calculateFinalAmount() in PrimeUser to apply a 50% delivery charge discount.
6.Read user type and order details from the user.
7.Create the appropriate object based on user type and display the order details.
```

## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber:  212222240008
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
import java.text.DecimalFormat;

class Order {
    String orderId;
    String customerName;
    double totalAmount;
    double deliveryCharge;

    public Order(String orderId, String customerName, double totalAmount, double deliveryCharge) {
        this.orderId = orderId;
        this.customerName = customerName;
        this.totalAmount = totalAmount;
        this.deliveryCharge = deliveryCharge;
    }

    double calculateFinalAmount() {
        return totalAmount + deliveryCharge;
    }

    void display(String userType) {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Order ID: " + orderId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("User Type: " + userType);
        System.out.println("Total Amount: " + totalAmount);
        System.out.println("Delivery Charge: " + deliveryCharge);
        System.out.println("Final Amount: " + df.format(calculateFinalAmount()));
    }
}


class NormalUser extends Order {

    public NormalUser(String orderId, String customerName, double totalAmount, double deliveryCharge) {
        super(orderId, customerName, totalAmount, deliveryCharge);
    }
}

class PrimeUser extends Order {

    public PrimeUser(String orderId, String customerName, double totalAmount, double deliveryCharge) {

        super(orderId, customerName, totalAmount, deliveryCharge);
    }
    @Override
    double calculateFinalAmount() {
  
        return totalAmount + (deliveryCharge * 0.5);
    }
}

public class FoodDeliveryApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String userType = sc.next();
        String orderId = sc.next();
        String customerName = sc.next();
        double totalAmount = sc.nextDouble();
        double deliveryCharge = sc.nextDouble();
        if (userType.equalsIgnoreCase("Normal")) {
            NormalUser user = new NormalUser(orderId, customerName, totalAmount, deliveryCharge);
            user.display("Normal");
        } else if (userType.equalsIgnoreCase("Prime")) {
            PrimeUser user = new PrimeUser(orderId, customerName, totalAmount, deliveryCharge);
            user.display("Prime");
        }

        sc.close(); 
    }
}
```





## OUTPUT:



## RESULT:
The program successfully calculates and displays the final payable amount for both Normal and Prime users using inheritance and overriding.

