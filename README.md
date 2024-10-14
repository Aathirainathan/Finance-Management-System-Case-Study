1)Sql Schema:
-

CREATE DATABASE Finance_Mgmt;
USE Finance_Mgmt;

CREATE TABLE Users (
    user_id INT PRIMARY KEY IDENTITY,
    username VARCHAR(50) UNIQUE NOT NULL,
    password VARCHAR(50) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL
);

CREATE TABLE ExpenseCategories (
    category_id INT PRIMARY KEY IDENTITY,
    category_name VARCHAR(50) NOT NULL
);

CREATE TABLE Expenses (
    expense_id INT PRIMARY KEY IDENTITY,
    user_id INT,
    amount DECIMAL(10, 2) NOT NULL,
    category_id INT,
    date DATE NOT NULL,
    description VARCHAR(255),
    FOREIGN KEY (user_id) REFERENCES Users(user_id),
    FOREIGN KEY (category_id) REFERENCES ExpenseCategories(category_id)
);

INSERT INTO ExpenseCategories (category_name)
VALUES ('Food'), ('Transportation'), ('Utilities'),('Investments');

INSERT INTO ExpenseCategories (category_name)
VALUES 
('Entertainment'),
('Healthcare'),
('Insurance'),
('Education'),
('Clothing'),
('Groceries'),
('Dining Out'),
('Subscriptions'),
('Travel'),
('Home Maintenance'),
('Personal Care'),
('Gifts'),
('Charity'),
('Pet Care'),
('Savings'),
('Debt Payments'),
('Fitness'),
('Electronics'),
('Rent'),
('Taxes');


2)Output Screenshots:
-

1.Add User:

![image](https://github.com/user-attachments/assets/925d6ade-661b-44ec-9c1c-96c3d5b2602e)

![image](https://github.com/user-attachments/assets/02e58864-a615-4d63-8f11-07874e0e56f9)

The user named ‘Krishna’ has been added to the database.

2.Login User:

![image](https://github.com/user-attachments/assets/aae23d22-17ad-4ff0-8f00-2fdbf88667bf)

The user got logged in and he can use the below displayed menu.

3.Add Expense:

![image](https://github.com/user-attachments/assets/b71a20b4-629b-4ff6-b54e-cacaa2c9f1f8)

![image](https://github.com/user-attachments/assets/7f81b4fe-e35b-4cca-a92f-c1072d4abcca)

![image](https://github.com/user-attachments/assets/ba8566ca-d58e-4319-ba92-a8fb712d4795)

![image](https://github.com/user-attachments/assets/da97ed06-36c5-4af3-adff-fb54957c164e)

All three expenses have been added to the Expenses table.

4.View All Expenses:

![image](https://github.com/user-attachments/assets/c4320039-e1f3-4c64-bcca-18ec3fcd77cc)

The user gets to view all the expenses he has made.

5.View Expenses by Category:

![image](https://github.com/user-attachments/assets/eea23a82-d421-4255-b0ca-6ecec05e7957)

Expenses under the category ‘Food’ is displayed to the user here.

6.View Expenses by Date Range:

![image](https://github.com/user-attachments/assets/44de2d34-2aa3-4494-9cb1-b9d916f5985a)

Here the user enters dates from 2024-10-10 to 2024-10-12 to get the expense made between those two dates and the user gets the expenses made.

7.Update Expense:

![image](https://github.com/user-attachments/assets/3f0947dd-b197-4a6d-bcb9-d47c35f2faf5)

Here the updated Expense of the user is successful and can be verified here.

8.Delete Expense:

![image](https://github.com/user-attachments/assets/04d73d6a-e66c-40a2-b254-6cba9da995a6)

![image](https://github.com/user-attachments/assets/8ce03aed-11f1-4000-9286-c8373648f2b5)

The expense has been successfully deleted here and is verified.

9.Logout:

![image](https://github.com/user-attachments/assets/94a1d39b-1297-4d5d-9c63-194f2987a963)

The user has been logged out successfully.

10.Delete User:

![image](https://github.com/user-attachments/assets/6c95a3e8-dd51-4f5e-bef4-844443efda93)

![image](https://github.com/user-attachments/assets/1622108a-35ff-42ae-96f8-f6d48c1440c4)
 
The user has been deleted successfully.


3)Exception Handling:
-
     
1.ExpenseNotFoundException:

![image](https://github.com/user-attachments/assets/8fafadff-a0b7-4d57-b779-930daf00eb3c)

Expection Id is not found.

2.UserNotFoundException:

![image](https://github.com/user-attachments/assets/5f3999c0-bd12-405b-950c-3d28c965d5a3)

NonExistentUser is not found.

4)Testing:
-

1.Test User Creation:

![image](https://github.com/user-attachments/assets/9cba07ad-6e74-4518-8122-8a9308c6030c)

2.Test Search Expense:

![image](https://github.com/user-attachments/assets/32900a31-70d3-4823-9fac-96cb1407f72b)

3.Test Expense Creation:

![image](https://github.com/user-attachments/assets/fb8e8aee-d6a8-4ce3-99ad-136f8be4a2d6)

4.Test Exceptions:

![image](https://github.com/user-attachments/assets/93793932-bb83-40b4-a252-27db9374e56b)
