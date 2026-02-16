# 🔍 Lookup Functions in Excel

This section covers one of the most important concepts in Excel for Data Analytics — **Lookup Functions**.

Lookup functions help us **find values from another table or range** based on a matching condition.  
They are widely used in real projects for joining data, fetching details, and building dashboards.

---

##  Why Lookup Functions Matter

In real-world datasets:

- Data is often spread across multiple tables  
- IDs exist in one sheet, details in another  
- Dashboards need values dynamically  

Lookup functions solve this problem by **connecting data together**.

---

## 1️⃣ VLOOKUP

### Purpose  
Searches for a value in the **first column** and returns related data from another column.

### Syntax

```excel
=VLOOKUP(lookup_value, table_array, column_index, FALSE)
```
``` Example =VLOOKUP(A2, D:F, 3, FALSE)```
- Finds value from column A
- Searches inside D:F
- Returns data from 3rd column
- FALSE = exact match
  
Limitations
- Works only left to right
- Breaks if columns move
- Less flexible for analytics

---
## 2️⃣ MATCH
Purpose - Returns the position (row or column number) of a value.

Syntax ```=MATCH(lookup_value, range, 0)```

Example ```=MATCH("John", A2:A20, 0)```  - MATCH only returns position — not the value.

 ---
## 3️⃣ INDEX
Purpose- Returns value from a specific row and column.

Syntax ```=INDEX(range, row_num, column_num)```

Example ```=INDEX(A2:C10, 3, 2)``` - Returns value from row 3, column 2.

---
## 4️⃣ INDEX + MATCH (Power Combination)

  Modern replacement of VLOOKUP.
  
  Why better?
- Works left & right
- Does not break when columns move
- More flexible
- Faster on large datasets

Example: Single Lookup ```=INDEX(B2:B20, MATCH(E2, A2:A20, 0))```
- MATCH finds row
- INDEX returns value

Example: Row + Column Lookup (2-Way Lookup) ```=INDEX(A1:J9, MATCH(F17,A1:A9,0),MATCH(G16,A1:J1,0))```


Used when:
- Both row and column are dynamic
- Timetable / matrix / dashboards

--- 
##  Practical Use Cases
- Employee salary lookup
- Product price fetch
- Grade assignment
- Dashboard filters
- Dynamic reporting

---
##  Key Learnings
- MATCH finds position
- INDEX returns value
- Combining both gives full control
- INDEX + MATCH is safer than VLOOKUP
- Essential skill for Data Analytics
