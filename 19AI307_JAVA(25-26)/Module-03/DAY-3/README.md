# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create abstract class BankAccount with method calculateInterest(). Extend it in SavingsAccount and FixedDepositAccount.
-  Input Format:
-  First line: 1 for SavingsAccount, 2 for FixedDepositAccount
- If 1: next line → balance (double)
- If 2: next line → amount (double) and years (int)
- Output Format:
- A single line showing interest earned rounded to 2 decimal places.
- For example:

| Input        | Result   |
|--------------|----------|
| 1 <br>10000  | 400.00   |
| 2 <br>50000 <br>2 | 7000.00 |


## AIM:
To write a Java program that demonstrates runtime polymorphism using an abstract class BankAccount and its subclasses to calculate interest for Savings and Fixed Deposit accounts.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the account type from the user.
4. If the user selects Savings, read balance and create a SavingsAccount object; otherwise, read amount and years to create a FixedDepositAccount object.
5. Store the object in the base class reference BankAccount.
6. Call the calculateInterest() method using runtime polymorphism.
7. Display the calculated interest.

## PROGRAM:
```txt
Program to implement a Abstraction using Java
Developed by: Sudharsanam R K
RegisterNumber:212222040163
```

## SOURCE CODE:
```java
import java.util.*;
abstract class BankAccount {
    abstract double calculateInterest();
}

class SavingsAccount extends BankAccount {
    double balance;
    SavingsAccount(double balance) {
        this.balance = balance;
    }
    double calculateInterest() {
        return balance * 0.04;
    }
}

class FixedDepositAccount extends BankAccount {
    double amount;
    int years;
    FixedDepositAccount(double amount, int years) {
        this.amount = amount;
        this.years = years;
    }
    double calculateInterest() {
        return amount * 0.07 * years;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int type = sc.nextInt();
        BankAccount account;
        if (type == 1) {
            double balance = sc.nextDouble();
            account = new SavingsAccount(balance);
        } else {
            double amount = sc.nextDouble();
            int years = sc.nextInt();
            account = new FixedDepositAccount(amount, years);
        }
        System.out.printf("%.2f", account.calculateInterest());
    }
}
```

## OUTPUT:
<img width="437" height="445" alt="image" src="https://github.com/user-attachments/assets/d5f40e48-7a38-4df5-9ce7-7c7bbda183a4" />

## RESULT:
The program successfully demonstrates runtime polymorphism using an abstract class. Depending on the account type entered by the user, the appropriate calculateInterest() method from the corresponding subclass is executed, and the interest amount is correctly displayed.

