<h1 align="center">TOPIC 05 - Database Management Systems & SQL</h1> <br>

### 1. What is the full meaning of SQL? List of the aggregate function. Write a SQL Query of a table and its output.

### SQL-এর Full Meaning

**SQL = Structured Query Language**

SQL হলো Database-এর **data create, read, update, delete এবং manage** করার জন্য ব্যবহৃত language।

### Aggregate Functions

Aggregate function একাধিক row-এর data নিয়ে **একটি result** দেয়।

| Function  | কাজ                     |
| --------- | ----------------------- |
| `COUNT()` | মোট row সংখ্যা গণনা করে |
| `SUM()`   | মোট যোগফল               |
| `AVG()`   | গড়                      |
| `MAX()`   | সর্বোচ্চ value          |
| `MIN()`   | সর্বনিম্ন value         |

### Example Table: `employees`

| id | name  | salary |
| -: | ----- | -----: |
|  1 | Rahim |  20000 |
|  2 | Karim |  30000 |
|  3 | Hasan |  25000 |
|  4 | Jamil |  35000 |

### SQL Queries

```sql
SELECT COUNT(*) AS total_employee
FROM employees;
```

**Output:**

| total_employee |
| -------------: |
|              4 |

```sql
SELECT SUM(salary) AS total_salary
FROM employees;
```

**Output:**

| total_salary |
| -----------: |
|       110000 |

```sql
SELECT AVG(salary) AS average_salary
FROM employees;
```

**Output:**

| average_salary |
| -------------: |
|          27500 |

```sql
SELECT MAX(salary) AS maximum_salary
FROM employees;
```

**Output:**

| maximum_salary |
| -------------: |
|          35000 |

```sql
SELECT MIN(salary) AS minimum_salary
FROM employees;
```

**Output:**

| minimum_salary |
| -------------: |
|          20000 |

### 🎯 Government Job Exam-এর জন্য মনে রাখুন

**SQL → Structured Query Language**

**Main Aggregate Functions → `COUNT, SUM, AVG, MAX, MIN`**

> **COUNT = কতটি, SUM = মোট, AVG = গড়, MAX = সবচেয়ে বেশি, MIN = সবচেয়ে কম**


<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>

## 2. Discuss about different types of relations in DBMS. 

## Types of Relationships in DBMS

DBMS-এ **Relationship** হলো দুই বা ততোধিক entity/table-এর মধ্যে সম্পর্ক।

প্রধানত **৩ ধরনের relationship** আছে:

| Type                      | Meaning                    | Example                     |
| ------------------------- | -------------------------- | --------------------------- |
| **1. One-to-One (1:1)**   | একজনের সাথে একজনের সম্পর্ক | একজন Person → একটি Passport |
| **2. One-to-Many (1:N)**  | একজনের সাথে অনেকের সম্পর্ক | একজন Teacher → অনেক Student |
| **3. Many-to-Many (M:N)** | অনেকের সাথে অনেকের সম্পর্ক | অনেক Student ↔ অনেক Course  |

### 1. One-to-One (1:1)

একটি table-এর একটি record অন্য table-এর **মাত্র একটি record-এর** সাথে সম্পর্কিত।

**Example:**
`Person → Passport`

একজন ব্যক্তির একটি Passport।

### 2. One-to-Many (1:N)

একটি record অন্য table-এর **অনেকগুলো record-এর** সাথে সম্পর্কিত হতে পারে।

**Example:**
`Department → Employees`

একটি Department-এ অনেক Employee থাকতে পারে।

### 3. Many-to-Many (M:N)

একটি table-এর অনেক record অন্য table-এর অনেক record-এর সাথে সম্পর্কিত হতে পারে।

**Example:**
`Students ↔ Courses`

একজন Student অনেক Course নিতে পারে এবং একটি Course অনেক Student নিতে পারে।

DBMS-এ Many-to-Many relationship সাধারণত একটি **Junction/Bridge table** ব্যবহার করে implement করা হয়।

### 🎯 Exam Focus

**Main types of relationships in DBMS:**

1. **One-to-One (1:1)**
2. **One-to-Many (1:N)**
3. **Many-to-Many (M:N)**

**মনে রাখার সহজ উপায়:**
`1 ↔ 1`, `1 ↔ Many`, `Many ↔ Many`


<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>


## 3. You are designing a database for a Library. Explain the relationship between a "Book" table and a "Borrower" table. Is it 1-to-1, 1-to-Many, or Many-to-Many? Justify your answer.

### Answer: Many-to-Many (M:N)

* একজন **Borrower** অনেকগুলো **Book** ধার নিতে পারে।
* একটি **Book** সময়ের সাথে অনেক **Borrower** ধার নিতে পারে।
* তাই **Book ↔ Borrower = Many-to-Many** relationship।
* এটি সাধারণত একটি **Borrowing/Junction table** দিয়ে implement করা হয়।

**Exam Answer:**

> The relationship between Book and Borrower is **Many-to-Many (M:N)** because one borrower can borrow many books and one book can be borrowed by many borrowers over time.


<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>

## 4. Assuming an Employees table with the structure: employee_id, employee_name,department_id and salary. (a) To find the total number of employees in each department. (b) To calculate the average salary across all employees in the organization.

### (a) Total employees in each department

```sql
SELECT department_id, COUNT(*) AS total_employees
FROM Employees
GROUP BY department_id;
```

**Key:** `COUNT()` + `GROUP BY`

### (b) Average salary of all employees

```sql
SELECT AVG(salary) AS average_salary
FROM Employees;
```

**Key:** `AVG()` calculates the average salary.


<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>


## 5. Suppose that we have a relational database with the following tables. Underlined attributes represent primary keys: Movies (mid, title, year); People (pid, name); Genres (gid, genre); HasRole (pid, mid, role); HasGenre (gid, mid). Write an SQL query to return the number of movies that are romantic comedies.

```
Suppose that we have a relational database with the following tables. Underlined attributes represent primary keys:
- Movies (mid, title, year)
- People (pid, name)
- Genres (gid, genre)
- HasRole (pid, mid, role)
- HasGenre (gid, mid)

Write an SQL query to return the number of movies that are romantic comedies.
```

### SQL Query

Romantic comedies = movies having **both** genres: `Romantic` and `Comedy`.

```sql
SELECT COUNT(DISTINCT m.mid) AS total_movies
FROM Movies m
JOIN HasGenre hg ON m.mid = hg.mid
JOIN Genres g ON hg.gid = g.gid
WHERE g.genre IN ('Romantic', 'Comedy')
GROUP BY m.mid
HAVING COUNT(DISTINCT g.genre) = 2;
```


<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>

## 6. Draw the ER diagram of the Library management system

![alt text](image.png)

![alt text](image-1.png)

![alt text](image-2.png)