# Data_Normalization_With_Excel-Power_Query-
This Project aims to showcase excel mastery in data normalization(removing redundancies) from a dataset using Microsoft Excel Power query.

### INTRODUCTION
The dataset in question is a retail store dataset. The company in this context has all their data on one single table which leads to excessive run time for queries and poor space management. we will attempt to use microsoft excel to normalize this dataset by removing as many redundancies as reasonably possible in order to help the company manage space in their database and to improve the efficiency of the database.

here's a preview of the initial dataset(Transactions.xlsx) below:

![image](https://github.com/user-attachments/assets/41241c89-566a-41c5-ac9e-0c2d01069972)

![image](https://github.com/user-attachments/assets/97629882-6526-4c92-8ca3-e1bc9c64f86f)

![image](https://github.com/user-attachments/assets/72ebce92-5927-4684-a16c-73cc643c8769)

Notice that all the columns are in one singular sheet and this makes it harder to navigate through the dataset since we are looking at a lot of things at once.

Normalization helps us to solve this problem because it helps us to cut out all redundancies from the dataset and make it more readable.


### WORK SCOPE
In this project we will:
1. #### 1NF: we will normalize the dataset to 1NF(first Normal Form) which just means that we will remove the major redundancies
2. #### 2NF: we will further normalize the dataset to 2NF where we will remove partial redundancies
3. #### 3NF: we will finally normalize the dataset to 3NF where we will remove all transitive redundancies
4. #### COMPARE AND ANALYZE: we will observe the difference between the initial dataset in terms of space occupied.

### 1NF
first we load the dataset into excel and then transform the data using power query
Then we make duplicates of the original data and then break down the main dataset into three tables for Transactions, Customers, Store and Product related data

For the customer table, we sort the customer id after removing duplicates
The screenshot below is the customer related data being isolated into a table called "Customers". The highlighted part shows that the customer id column is an appropriate primary key.
here's a preview of the customers table
![snap 1](https://github.com/user-attachments/assets/9f8bb3cd-4f8b-4055-91bf-52ac1976c429)

Similarly, we repeat the same process for Store related data.

![snap 2](https://github.com/user-attachments/assets/31770925-2c10-464d-bac0-30cbda11cebe)

and finally for Product related data,

![snap 3](https://github.com/user-attachments/assets/10218302-4f2b-4e71-9c6d-64ea6650f213)

the Transactions table will hold the remaining columns
here's a simple view of the current database design after 1NF Normalization

![snap 4](https://github.com/user-attachments/assets/7cee8cce-3b7b-4a40-9f2a-b3377fdc594a)

### 2NF
The goal of second Normal Form is to remove partial dependencies(where the redundant columns only depand on a small part of the primary key)

We can further split the Transactions table into two other tables called "Orders" and "Order_Line_items" as shown below

![snap 5](https://github.com/user-attachments/assets/7ca4b2a6-fd66-441f-846b-126f57b1edd6)

### 3NF
The goal of Third Normal form is to remove transitive dependencies.

in this phase we will split the "Products" table into SubCategories and Categories

Here's what the current schema looks like on power pivot:

![snap 7](https://github.com/user-attachments/assets/46a4d932-3ae3-4aeb-b1c3-50189b4e3676)

### COMPARE AND ANALYZE

here's a screenshot showing the initial "Transactions" dataset and the Normalized dataset so we can compare the space used

![image](https://github.com/user-attachments/assets/9e549746-247e-48e4-bc96-1e2d680dfa14)

Notice that due to our normalization efforts, the size of the entire dataset reduced by about 30%!!

The time taken to load queries also improved significantly

Here's what the dataset looks lke now

![image](https://github.com/user-attachments/assets/e8dbcaf5-30fd-4f20-8bd7-4094e4ea24c5)

Notice how we went from only one messy sheet to 7 smaller, more readable datasets as part of an excel workbook



### CONCLUSION
Data Normalization is an important part of every day analytics since data needs to be properly formatted before it can be analyzed


