# ATM Interface Project 

## 1. Introduction

This report presents the development and implementation of an advanced ATM (Automated Teller Machine) interface using Python. The project was undertaken as part of a Python Programming internship, with the goal of creating a fully functional ATM interface within a 7-day timeframe.

### 1.1 Project Objectives

- Develop a functional ATM interface using Python
- Implement core banking operations (balance inquiry, withdrawal, deposit, transfer)
- Enhance the basic functionality with advanced features
- Demonstrate proficiency in Python programming and software development concepts

### 1.2 Technologies Used

- Python 3.x
- SQLite for database management
- Matplotlib for data visualization
- Jupyter Notebook for development and presentation

## 2. System Design

### 2.1 Architecture Overview

The ATM interface is designed with a modular architecture, separating core functionalities into distinct functions. The system uses a SQLite database for persistent storage of account information and transactions.

### 2.2 Database Schema

Two main tables are used in the database:

1. `accounts` table:
   - `account_number` (Primary Key)
   - `pin_hash`
   - `balance`
   - `name`

2. `transactions` table:
   - `id` (Primary Key)
   - `account_number`
   - `type`
   - `amount`
   - `timestamp`
   - `category`

### 2.3 Security Considerations

- PINs are hashed using SHA-256 before storage
- Sensitive input (PINs) uses the `getpass` module to mask input

## 3. Implementation Details

### 3.1 Core Functions

1. `check_balance(account)`: Retrieves and displays the current balance
2. `withdraw(account)`: Handles cash withdrawal
3. `deposit(account)`: Processes cash deposits
4. `transfer(account)`: Manages fund transfers between accounts
5. `log_transaction(account, transaction_type, amount)`: Records all transactions
6. `view_transactions(account)`: Displays recent transactions
7. `visualize_spending(account)`: Generates a pie chart of spending by category
8. `change_pin(account)`: Allows users to change their PIN

### 3.2 Main Interface

The `atm_interface()` function serves as the main program loop, handling user authentication and menu navigation.

### 3.3 Data Visualization

The spending visualization feature uses Matplotlib to create a pie chart, offering users a graphical representation of their spending patterns.

## 4. Advanced Features

### 4.1 Database Integration

Unlike basic implementations that use in-memory data structures, this project uses SQLite for persistent storage. This allows for data retention between sessions and demonstrates database management skills.

### 4.2 Transaction Categorization

Users can categorize each transaction, enabling more detailed financial tracking and analysis.

### 4.3 Spending Visualization

The system can generate a pie chart of user spending by category, providing valuable insights into spending habits.

### 4.4 Enhanced Security

PINs are securely hashed before storage, and users can change their PINs. This demonstrates an understanding of basic security practices in financial systems.

## 5. Challenges and Solutions

### 5.1 Database Management

Challenge: Implementing a persistent storage solution.
Solution: Utilized SQLite, a lightweight database that doesn't require a separate server process.

### 5.2 Security Implementation

Challenge: Storing PINs securely.
Solution: Implemented PIN hashing using the SHA-256 algorithm.

### 5.3 Data Visualization

Challenge: Providing user-friendly insights into spending habits.
Solution: Integrated Matplotlib to create visual representations of transaction data.

## 6. Future Enhancements

Several potential improvements have been identified for future development:

1. Graphical User Interface (GUI): Implement a user-friendly GUI using libraries like Tkinter or PyQt.
2. Multi-Currency Support: Add functionality to handle multiple currencies and perform conversions.
3. Scheduled Transactions: Implement features for setting up recurring payments or transfers.
4. Account Types: Introduce different types of accounts (e.g., savings, checking) with varying interest rates.
5. Web Interface: Develop a web-based version of the ATM interface using frameworks like Flask or Django.

## 7. Conclusion

This project successfully delivered a fully functional ATM interface with several advanced features, meeting and exceeding the initial project requirements. The implementation demonstrates proficiency in Python programming, database management, security considerations, and data visualization.

The modular design of the system allows for easy maintenance and future enhancements. The inclusion of advanced features like spending visualization and transaction categorization adds significant value to the basic ATM functionality.

This project has provided valuable experience in software development practices, database integration, and creating user-centric financial applications.

## 8. References

1. Python Documentation: https://docs.python.org/3/
2. SQLite Documentation: https://www.sqlite.org/docs.html
3. Matplotlib Documentation: https://matplotlib.org/stable/contents.html

## Appendix: User Guide

### A.1 Getting Started

1. Ensure Python 3.x is installed on your system.
2. Install required libraries: `pip install matplotlib`
3. Run the Jupyter notebook containing the ATM interface code.

### A.2 Using the ATM Interface

1. Start the interface by running the `atm_interface()` function.
2. Enter your account number and PIN when prompted.
3. Choose from the available options:
   - Check Balance
   - Withdraw
   - Deposit
   - Transfer
   - View Recent Transactions
   - Visualize Spending
   - Change PIN
   - Logout
4. Follow the on-screen prompts for each operation.
5. For security, always remember to log out when you're done.

### A.3 Tips for Use

- Keep your PIN secure and change it regularly.
- Categorize your transactions accurately for better spending insights.
- Review your recent transactions and spending visualization regularly to track your financial habits.
