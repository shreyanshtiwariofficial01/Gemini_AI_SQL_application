# 📌 Gemini SQL Query Generator (with SQLite + Streamlit)

This project uses **Google Gemini** to convert **natural language questions** into **SQL queries**, runs them on an SQLite database, and displays the results using **Streamlit**.

There are two main files:

1. **sql.py** – creates the SQLite database (`Naresh_it_employee.db`) and inserts sample employee records.
2. **main_app.py** – the Streamlit application that accepts user questions, converts them to SQL using Gemini, executes the query, and displays results.

---

## 📁 Project Structure

├── sql.py # Creates DB & inserts sample data

├── main_app.py # Streamlit + Gemini main application

├── Naresh_it_employee.db # Auto-created SQLite database

├── .env # Store your GEMINI_API_KEY here

├── requirements.txt

└── README.md

---


# 🚀 Features

### ✔ Create SQLite database automatically 

`sql.py` will generate a database with columns:

- `employee_name`
- `employee_role`
- `employee_salary`

### ✔ Insert sample employee data  
Contains 6 sample employee records for testing.

### ✔ Natural Language → SQL conversion  
Gemini interprets user questions like:
> “Show me all Data Science employees.”

and generates SQL like:

- SELECT * FROM employeee_table WHERE employee_role='Data Science';

---

### How It Works

- User enters a question in plain English

- Gemini converts it to SQL (based on given prompt)

- SQLite executes the SQL

- Results appear in Streamlit
