# Java Bank Account System

A Java implementation of a simple bank account system demonstrating **Object-Oriented Programming** concepts such as inheritance, encapsulation, and polymorphism.

---

## Project Structure

```
Java-BankAccount/
├── BankAccount.java       # Base class for all bank accounts
├── CheckingAccount.java   # Subclass for checking accounts
├── SavingsAccount.java    # Subclass for savings accounts
└── README.md
```

---

## Class Overview

### `BankAccount` (Base Class)

The foundation class that models a generic bank account.

| Member | Type | Description |
|---|---|---|
| `accountNumber` | `String` | Unique identifier for the account |
| `accountName` | `String` | Name of the account holder |
| `balance` | `double` | Current account balance (starts at `0.0`) |

**Methods:**

| Method | Return Type | Description |
|---|---|---|
| `BankAccount(accNumber, accName)` | Constructor | Creates a new account with balance `0.0` |
| `getAccountName()` | `String` | Returns the account holder's name |
| `getAccountNumber()` | `String` | Returns the account number |
| `getBalance()` | `double` | Returns the current balance |
| `deposit(amount)` | `boolean` | Deposits amount; returns `true` on success |
| `withdraw(amount)` | `boolean` | Withdraws amount; returns `false` if insufficient funds |

---

### `CheckingAccount` (Subclass)

Extends `BankAccount` with checking account-specific behaviour.

---

### `SavingsAccount` (Subclass)

Extends `BankAccount` with savings account-specific behaviour (e.g. interest logic).

---

## Key OOP Concepts Demonstrated

- **Encapsulation** — Private fields accessed via public getters
- **Inheritance** — `CheckingAccount` and `SavingsAccount` extend `BankAccount`
- **Polymorphism** — Subclasses override or extend base behaviour

---

## How to Run

### Prerequisites
- Java JDK 8 or higher

### Compile

```bash
javac BankAccount.java CheckingAccount.java SavingsAccount.java
```

### Run

```bash
java BankAccount
```

---

## Example Usage

```java
BankAccount account = new BankAccount("ACC001", "Manoj Pentapati");

account.deposit(1000.0);   // returns true
account.withdraw(400.0);   // returns true
account.withdraw(700.0);   // returns false — insufficient funds

System.out.println(account.getBalance()); // 600.0
```

---

## Author

**Manoj Pentapati**

---

## License

This project is open source and available for educational purposes.
