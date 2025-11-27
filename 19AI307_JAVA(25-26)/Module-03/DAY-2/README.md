# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Create a base class BankAccount with methods deposit() and withdraw().

Create two subclasses:

SavingsAccount: allows withdrawal but limits it to ₹10,000 per transaction.

CheckingAccount: allows withdrawal with a ₹10 fee per transaction.

Input account type, deposit amount, and withdrawal amount from the user.

If checking account has insufficient balance print - "Insufficient balance in CheckingAccount (including ₹10 fee)."

## AIM:
To demonstrate method overriding by performing deposit and withdrawal operations on Savings and Checking accounts.

## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a BankAccount class with deposit and withdraw methods.
4.Create SavingsAccount and CheckingAccount classes that override the withdraw method with specific rules.
5.Read the account type, deposit amount, and withdrawal amount from the user.
6.Create the appropriate account object based on the account type.
7.Perform deposit, perform withdrawal, and display the final balance.

```



## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber:  212222240008
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
        double fee = 10;
        double total = amount + fee;
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

        String accountType = sc.nextLine().toLowerCase();
        double depositAmount = sc.nextDouble();
        double withdrawAmount = sc.nextDouble();

        BankAccount account;

        if (accountType.equals("savings")) {
            account = new SavingsAccount();
        } else if (accountType.equals("checking")) {
            account = new CheckingAccount();
        } else {
            System.out.println("Invalid account type.");
            sc.close();
            return;
        }

        account.deposit(depositAmount);
        account.withdraw(withdrawAmount);
        System.out.printf("Final Balance: ₹%.2f%n", account.balance);

        sc.close();
    }
}
```





## OUTPUT:

<img width="1302" height="421" alt="image" src="https://github.com/user-attachments/assets/cdf6d2bb-6c40-4449-8868-250ae79d3a19" />


## RESULT:
The program successfully applies different withdrawal rules for Savings and Checking accounts using method overriding and displays the final balance.

