
# 📧 Server Log Data Extraction and User History Database Update

## 📌 Project Overview
This project focuses on extracting meaningful information from a **server log file (`mbox.txt`)**, transforming the extracted data into a structured format, and storing it in both **NoSQL (MongoDB Atlas)** and **Relational (SQLite)** databases.

The project demonstrates a real-world **Data Engineering pipeline** involving:
- Log file parsing using **Regular Expressions**
- Data cleaning and transformation
- Multi-database integration (MongoDB ➜ SQLite)
- Analytical querying using **SQL**

The entire workflow is implemented and executed on **Google Colab**.

---

## 🧰 Technologies Used
- **Programming Language:** Python  
- **Execution Platform:** Google Colab  
- **Databases:**
  - MongoDB Atlas (NoSQL)
  - SQLite (Relational Database)
- **Query Language:** SQL  
- **Text Processing:** Regular Expressions (Regex)

---

## 📂 Project Structure
server-log-etl/
│
├── mbox.txt # Input server log file
├── user_history.db # SQLite database output
├── queries.txt # SQL queries for analysis
├── Mini Project 2.ipynb # Google Colab notebook
└── README.md # Project documentation

## 📥 Dataset Description
- **Dataset Name:** `mbox.txt`
- **Type:** Server log file
- **Content:** Email communication logs containing email addresses and timestamps
- **Usage:** Source data for extracting user email history

---

## 🎯 Problem Statement
The objective of this project is to:
- Extract **email addresses** and their associated **timestamps** from a server log file
- Clean and standardize the extracted data
- Store the processed data in a **MongoDB collection**
- Transfer the data into a **relational SQLite database**
- Perform analytical queries to gain insights into user email activity

---

## 🛠️ Task Breakdown

### 🔹 Task 1: Extract Email Addresses and Dates
- Read the `mbox.txt` file line by line
- Use **Regex** to identify valid email addresses
- Extract corresponding date and time information

---

### 🔹 Task 2: Data Transformation
- Structure the extracted data into tabular format
- Standardize the date format to:
YYYY-MM-DD HH:MM:SS

- Remove duplicates and invalid records

---

### 🔹 Task 3: Save Data to MongoDB
- Connect to **MongoDB Atlas**
- Create a collection named:
user_history
- Insert transformed records into MongoDB for persistence

---

### 🔹 Task 4: Database Connection and Data Upload
- Fetch records from MongoDB
- Connect to SQLite using Python
- Create a relational table:
user_history
- Apply constraints:
- Primary Key
- NOT NULL constraints where applicable
- Insert records into the SQLite database

**Output Database:**
user_history.db

---

### 🔹 Task 5: SQL Analysis & Queries
- Execute SQL queries on the SQLite database to analyze email activity
- All queries are stored in:
queries.txt

#### Example Analytical Questions
1. List all unique email addresses  
2. Count the number of emails received per day  
3. Find the first and last email date for each email address  
4. Count the total number of emails per domain (gmail.com, yahoo.com, etc.)  
5. Identify the most active email sender  
6. Count emails per month  
7. Find days with the highest email traffic  
8. Count distinct domains  
9. Identify inactive users  
10. Rank email addresses by activity  

---

## ▶️ How to Run the Project (Google Colab)

1. Open **Google Colab**
2. Upload the notebook `etl_pipeline.ipynb`
3. Upload `mbox.txt` to the Colab environment
4. Configure MongoDB Atlas connection string
5. Run all notebook cells sequentially
6. Verify output files:
 - `user_history.db`
 - `queries.txt`

---

## 📄 Output Artifacts

### 📌 SQLite Database
- **File:** `user_history.db`
- **Table:** `user_history`
- **Purpose:** Relational storage and analytical querying

### 📌 SQL Queries
- **File:** `queries.txt`
- **Purpose:** Contains all SQL queries required for analysis

## 👤 Author
**Gayatri**  
Python Backend Engineer | Data Engineering Enthusiast  
