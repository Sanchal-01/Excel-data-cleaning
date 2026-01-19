# 📊 Excel for Data Analytics

This repository contains my **self-made Excel notes and practice work** created while learning
**Microsoft Excel for Data Analytics**.

All topics covered here are based on my **personal handwritten notes, class learning, and hands-on Excel practice**.
The focus is on understanding **data cleaning, logical functions, and dynamic Excel formulas**
used in real-world analytics tasks.

---

## 🎯 Purpose of This Repository

- Build strong fundamentals of Excel for Data Analytics
- Learn practical data cleaning and preprocessing techniques
- Understand Excel formulas used in analysis and reporting
- Prepare for interviews and real-world analytics work

---

## 📚 Topics Covered (As Studied)

### 1️⃣ Excel Basics & Interface
- Excel interface overview (Ribbon, Tabs, Formula Bar, Name Box)
- Workbook and Worksheet concepts
- Cells, ranges, and basic navigation
- Sheet operations (insert, rename, protect)

---

### 2️⃣ Data Entry & Formatting
- Creating serial numbers (normal, odd, even)
- Fill handle and auto-fill techniques
- Adjusting row height and column width
- Cell alignment, borders, and formatting
- Date and number formatting (`Ctrl + 1`)
- Using `RANDBETWEEN()` for random values

---

### 3️⃣ Cell References
- Relative cell references
- Absolute cell references (`$A$1`)
- Mixed cell references
- Practical use cases in formulas

---

### 4️⃣ Data Cleaning Techniques
This section focuses on cleaning **raw and messy datasets**.

- Removing duplicate records
- Removing blank rows using filters
- Handling extra spaces using `TRIM()`
- Fixing non-breaking spaces using:
```excel
=TRIM(SUBSTITUTE(A1, CHAR(160), ""))
```
- Changing text case:
- `UPPER()`
- `LOWER()`
- `PROPER()`
- Handling negative values using `IF()`

---

### 5️⃣ Logical Functions
- `IF()`
- Nested `IF`
- `IFS()`
- `AND()`
- `OR()`

Used for:
- Conditional decisions
- Incentive calculations
- Eligibility checks

---

### 6️⃣ Dynamic Array Functions
- `SORT()`
- `FILTER()`
- `TAKE()`
- Combining dynamic functions for analysis

Example use cases:
- Top / bottom performers
- Condition-based data extraction
- Dynamic reporting

---

### 7️⃣ Lookup Functions (Upcoming)
- VLOOKUP
- INDEX
- MATCH

*(Will be added as learning progresses)*

---

## 📂 Repository Structure
```bash
excel-data-cleaning/
│
├── README.md
│
├── 01-data-cleaning-basics/
│ ├── README.md
│ └── handwritten-notes/
│
├── 02-logical-functions/
│ ├── README.md
│ └── handwritten-notes/
│
├── 03-dynamic-array-functions/
│ ├── README.md
│ └── handwritten-notes/
│
├── datasets/
│ ├── raw/
│ └── cleaned/
│
└── resources/
└── references.md
```
---

## 📝 Note

- All notes are based on **personal study and practice**
- Handwritten notes and examples are uploaded topic-wise
- Content is added gradually as part of my learning journey

---

## 👤 Author

**Sanchal Kumar**  
(Data Analytics – Excel Fundamentals)

