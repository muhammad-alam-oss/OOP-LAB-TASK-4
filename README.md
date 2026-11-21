# OOP-LAB-TASK-4

Bank Accounts (Java)

A small Java console program I made to practice inheritance and method overriding. It models a simple bank with a general account, a savings account and a current account.

All bank accounts have a holder name and a balance, so those live in a parent class called Account. The savings and current accounts extend it and each one prints its own extra information.

How it's set up

Account is the parent class. It stores the holder name and the balance, and has a displayInfo() method that prints both.

Savingsaccount extends Account. It has an interestRate field set to 0.5 (percent). It overrides displayInfo(): first it prints a heading, then calls super.displayInfo() for the name and balance, and then shows the interest rate and the profit, which is calculated as balance * interestRate / 100.

Currentaccount extends Account too, but it's simpler. It overrides displayInfo() to print a heading, the usual details from the parent, and a line saying there's no interest.

Bank is the main class. It creates one account of each type and calls displayInfo() on all three. Each object prints something different even though the method name is the same.

What it prints
Account holder name = Alam
Account balance = 50000.0
...Savingsaccount...
Account holder name = Ali
Account balance = 20000.0
 Interest on saving = 0.5%, Profit= 100.0
...Currentaccount...
Account holder name = Mahmood
Account balance = 80000.0
 no interest
