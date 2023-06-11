# SQL - EXPERIMENT 6 - SET OPERATIONS
## AIM:
The aim of this program is to perform set operations (Union, Union All, Intersect, and Except) between two tables, A and B, in order to combine, find common elements, or identify differences between the tables.

## ALGORITHM:
1. Create table A with attributes ID and name.
2. Create table B with attributes ID and name.
3. Insert values into table A.
4. Insert values into table B.
5. Display the contents of table A.
6. Display the contents of table B.
7. Perform set operations: 
        a. Union: Combine rows from table A and table B, eliminating duplicates. 
        b. Union All: Combine rows from table A and table B, including duplicates. 
        c. Intersect: Find common rows between table A and table B. 
        d. Except: Find rows in table A that do not exist in table B.
8. Display the results of each set operation.

## PROGRAM:
```
create database if not exists MyDatabase;
use MyDatabase;
CREATE TABLE A (
  ID INTEGER PRIMARY KEY,
  name TEXT
);

CREATE TABLE B (
  ID INTEGER PRIMARY KEY,
  name TEXT
);

-- Insert values into table A
INSERT INTO A VALUES (1, 'John');
INSERT INTO A VALUES (2, 'Alice');
INSERT INTO A VALUES (3, 'Bob');

-- Insert values into table B
INSERT INTO B VALUES (2, 'Alice');
INSERT INTO B VALUES (3, 'Bob');
INSERT INTO B VALUES (4, 'Charlie');

-- Display table A
SELECT * FROM A;

-- Display table B
SELECT * FROM B;

SELECT * FROM A
UNION
SELECT * FROM B;

SELECT * FROM A
UNION ALL
SELECT * FROM B;

SELECT * FROM A
INSERTSET;
SELECT * FROM B;

SELECT * FROM A
EXCEPT
SELECT * FROM B;
```

## OUTPUT:
### The output for table A will be:
![image](https://github.com/Shavedha/SQL-EXP-6/assets/93427376/90b0ff22-df41-419a-8d19-8c56f899e9b7)

### The output for table B will be:
![image](https://github.com/Shavedha/SQL-EXP-6/assets/93427376/4f318880-f68f-40a9-be6f-755415d8d9d2)

### Union:
![image](https://github.com/Shavedha/SQL-EXP-6/assets/93427376/e74a0cde-2930-4e21-bbf4-9f5d9416cec4)

### Union All:
![image](https://github.com/Shavedha/SQL-EXP-6/assets/93427376/ec2f1fec-3407-4ba3-b4bc-5f22ba77fc9d)

### Intersect:
![image](https://github.com/Shavedha/SQL-EXP-6/assets/93427376/dc46805a-7ee9-47b5-960e-da692ceda729)
### Except:
![image](https://github.com/Shavedha/SQL-EXP-6/assets/93427376/600b7261-a15a-4a18-bd8a-b1ed31ad0c89)

## RESULT:
These results illustrate the outcomes of the set operations performed on tables A and B.
