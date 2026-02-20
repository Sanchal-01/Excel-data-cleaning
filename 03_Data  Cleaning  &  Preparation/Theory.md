# 🧹 Chapter 3 – Data Cleaning & Preparation

This chapter focuses on cleaning raw and messy datasets to make them ready for analysis.  
Data cleaning is one of the most important skills for any Data Analyst because dirty data leads to wrong insights.

---

## 🎯 Goal of This Chapter

- Remove duplicate and blank records  
- Fix spacing and formatting issues  
- Standardize text cases  
- Handle negative values  
- Split combined data into structured columns  
- Apply data validation rules  

---

## ✅ Topics Covered

---

### 1. Removing Duplicate Rows

Used to remove entire duplicate records from a dataset.

Steps:

- Select complete table  
- Go to **Data → Data Tools → Remove Duplicates**  
- Keep all columns checked  
- Click OK  

Removes fully duplicated rows.

---

### 2. Removing Duplicate Values in a Single Column

Example: Duplicate phone numbers.

Steps:

- Select target column  
- Data → Remove Duplicates  
- Uncheck all → Select only required column  
- Click OK  

Removes duplicates only from that column.

---

### 3. Removing Blank Rows (Using Filter)

Steps:

1. Select header row  
2. Data → Filter  
3. Open dropdown of any filled column  
4. Select **(Blanks)**  
5. Select visible rows  
6. Right click → Delete rows  
7. Turn OFF filter  

All blank rows removed.

---

### 4. Removing Extra Spaces (TRIM Function)

Two types of spaces:

- Leading space (before text)  
- Trailing space (after text)  

Formula:

```excel
=TRIM(A1)
```
- Removing Non-Breaking Spaces (Important)
- Copied data from PDFs or websites may contain hidden spaces.
- Use:
```
=TRIM(SUBSTITUTE(A1, CHAR(160), ""))
```
Explanation:
- CHAR(160) → Non-breaking space
- SUBSTITUTE replaces it
- TRIM removes extra spaces
---

### 5. Changing Text Case

Excel functions used:

- Proper Case =PROPER(A1)
- Upper Case =UPPER(A1)
- Lower Case =LOWER(A1)

After applying formulas:
    - Copy column  
    - Paste Special → Values  

(This removes formula dependency)

---

### 6.  Handling Negative Values

Formula: ```=IF(stock<0,0,stock)```

Purpose:
- Converts negative values into zero  
- Keeps positive values unchanged  

Used while cleaning numeric datasets.

---

### 7. Splitting Data into Columns

#### Text to Columns
Used to split data using space or comma.

Example: Rohit Sharma → Rohit | Sharma  

Steps:
- Select column  
- Go to Data → Text to Columns  
- Choose delimiter  
- Finish  



#### Dynamic Name Split Using Formulas

First Name:```=LEFT(A2,FIND(" ",A2)-1)```

Last Name:```=MID(A2,FIND(" ",A2)+1,LEN(A2))```

This method is dynamic and reusable.

---

### 8. Data Validation

Used to restrict user input.

Examples:
- Age between 18–60  
- Dropdown list for departments  
- Email validation  

Steps:
- Select cell  
- Go to Data → Data Validation  
- Choose rule  
- Click OK  

Helps maintain clean and consistent datasets.

---

## 🧠 Key Learnings from Chapter 3

- Clean data improves analysis accuracy  
- Remove duplicates and blanks first  
- Fix spaces before lookups  
- Convert formulas to values  
- Split columns properly  
- Apply validation rules  

---
