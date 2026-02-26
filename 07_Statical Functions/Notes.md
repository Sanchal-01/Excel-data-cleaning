# Statistical Functions in Excel

##  Overview

Statistical functions in Excel help answer three critical business questions:

- How much? (Total)
- How many? (Count)
- How good? (Average / Best / Worst)

These functions are widely used in dashboards, KPI calculations, performance analysis, and real-world business reporting.

Covered Functions:
SUMIF | SUMIFS  
COUNTIF | COUNTIFS  
AVERAGEIF | AVERAGEIFS  
MAXIFS | MINIFS  

---

# 1️⃣ SUMIF & SUMIFS

## 🔹 SUMIF

Used to calculate the total (sum) of values that meet **one condition**.

### Syntax:
```=SUMIF(range, criteria, [sum_range])```


### Example:
Total sales for Maharashtra:
```=SUMIF(State_Column, "Maharashtra", Sales_Column)```

---

## 🔹 SUMIFS

Used to calculate total based on **multiple conditions**.
### Syntax: 
```=SUMIFS(sum_range, criteria_range1, criteria1, criteria_range2, criteria2, ...)```
### Example:
Total sales of "Table" product in Maharashtra:<br>
```=SUMIFS(Sales_Column, State_Column, "Maharashtra", Product_Column, "Table")```

---

# 2️⃣ COUNTIF & COUNTIFS

## 🔹 COUNTIF
Counts number of records that meet **one condition**.
### Syntax:
```=COUNTIF(range, criteria)```

### Example:
Number of transactions in Maharashtra:
```=COUNTIF(State_Column, "Maharashtra")```


---

## 🔹 COUNTIFS
Counts records based on **multiple conditions**.

### Syntax:
```=COUNTIFS(range1, criteria1, range2, criteria2, ...)```

### Example:
Number of Table transactions in Maharashtra:<br>
```=COUNTIFS(State_Column, "Maharashtra", Product_Column, "Table")```


###  Use Cases:
- Finding number of orders
- Validating average calculations
- Sanity checking totals

---

# 3️⃣ AVERAGEIF & AVERAGEIFS

## 🔹 AVERAGEIF

Calculates average based on **one condition**.

### Syntax:
```=AVERAGEIF(range, criteria, average_range)```

### Example:
Average sales in Maharashtra:
```=AVERAGEIF(State_Column, "Maharashtra", Sales_Column)```



---

## 🔹 AVERAGEIFS
Calculates average based on **multiple conditions**.

### Syntax:
```=AVERAGEIFS(average_range, criteria_range1, criteria1, ...)```


### Example:
Average sales of Table in Maharashtra:
```=AVERAGEIFS(Sales_Column, State_Column, "Maharashtra", Product_Column, "Table")```


---

## Analyst Rule (Very Important)
- Average = Total ÷ Count
- Always cross-check: ```=SUMIFS(...) / COUNTIFS(...)```
This ensures data validation accuracy.

---

# 4️⃣ MAXIFS

Returns the highest value based on condition(s).

### Syntax:
```=MAXIFS(max_range, criteria_range1, criteria1, ...)```

### Example:
Highest sales in Maharashtra:
```=MAXIFS(Sales_Column, State_Column, "Maharashtra")```

 Note: MAXIF is not directly available in older Excel versions.

---

# 5️⃣ MINIFS

Returns the lowest value based on condition(s).
### Syntax: 
```=MINIFS(min_range, criteria_range1, criteria1, ...)```

### Example:
Lowest sales of Table in Maharashtra:
```=MINIFS(Sales_Column, State_Column, "Maharashtra", Product_Column, "Table")```


---

#  Quick Revision Summary

| Function | Purpose |
|----------|---------|
| SUMIF / SUMIFS | Total value |
| COUNTIF / COUNTIFS | Number of records |
| AVERAGEIF / AVERAGEIFS | Mean value |
| MAXIFS | Highest value |
| MINIFS | Lowest value |

---

#  Common Mistakes (Important)

- Using COUNT instead of COUNTIF
- Using SUMIF to calculate average
- Criteria mismatch between SUMIFS & COUNTIFS
- Not validating average using Total ÷ Count

---

#  When to Use These Functions

- Sales analysis
- State / product performance tracking
- Dashboard KPI calculations
- Interview & exam questions
- Real-world data validation

---

#  One-Line Power Takeaway

Statistical functions help answer:
“How much?”, “How many?”, and “How good?” in data.
