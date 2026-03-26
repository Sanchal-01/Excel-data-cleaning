# 📅 Chapter 8: Date Formulas in Excel

> **Topic Covered:** `DAY` `MONTH` `YEAR` `DATE` `TEXT` `EOMONTH` `DATEDIF` `NETWORKDAYS.INTL`

---
## 1. DATE Function

### Purpose
The `DATE` function is used to **construct a valid Excel date** using separate Year, Month, and Day values.

### Syntax
```excel
=DATE(year, month, day)
```

### Example
```excel
=DATE(YEAR(B2), MONTH(B2), DAY(B2))
```
> Extracts year, month, and day from an existing date and rebuilds it into a proper Excel-recognized date.

###  Use Cases
- Fix text-formatted dates
- Normalize inconsistent date formats
- Date transformation during data cleaning

---

## 2. Days Difference (End Date - Start Date)

###  Purpose
To calculate the **number of days between two dates**.

### Formula
```excel
= End_Date - Start_Date
= C2 - B2
```

> 💡 Excel stores dates as serial numbers internally, so subtracting two dates directly gives the number of days between them.

###  Use Cases
- Project duration calculation
- Days remaining till deadline
- Timeline analysis

---

## 3. DATEDIF – Age in Years

###  Purpose
To calculate **completed years** between two dates (most commonly used for age calculation).

### Syntax
```excel
=DATEDIF(start_date, end_date, "Y")
```

### Example
```excel
=DATEDIF(D2, TODAY(), "Y") & " Years"
```

| Unit Code | Meaning |
|-----------|---------|
| `"Y"` | Completed years only (ignores months & days) |

###  Use Cases
- Employee age calculation
- Years of experience

---

## 4. DATEDIF – Exact Age in Years, Months & Days

###  Purpose
To calculate **exact age** broken down into Years + Months + Days.

### Formula Used
```excel
=DATEDIF(D2, TODAY(), "Y")  & " Years "
& DATEDIF(D2, TODAY(), "YM") & " Months "
& DATEDIF(D2, TODAY(), "MD") & " Days"
```

### Unit Code Breakdown

| Unit Code | Meaning |
|-----------|---------|
| `"Y"` | Completed years |
| `"YM"` | Remaining months after completed years |
| `"MD"` | Remaining days after completed months |

###  Use Cases
- HR reports with exact tenure
- Accurate age calculation for records

---

## 5. TEXT Function (Date to Text)

###  Purpose
To **convert a date or number into a formatted text string** for display or reporting purposes.

### Syntax
```excel
=TEXT(value, format_text)
```

### Example
```excel
=TEXT(C14, "DD-MMM-YYYY")
```
**Output:** `03-Feb-2026`

### Common Format Codes

| Format Code | Output Example |
|-------------|----------------|
| `"DD-MM-YYYY"` | 03-02-2026 |
| `"DD-MMM-YYYY"` | 03-Feb-2026 |
| `"MMMM YYYY"` | February 2026 |
| `"DDD"` | Mon |

###  Use Cases
- Reporting & dashboards
- Exporting data to other tools
- User-friendly date display

---

## 6. EOMONTH Function

### Purpose
To find the **last date of a month**, a given number of months before or after a starting date.

### Syntax
```excel
=EOMONTH(start_date, months)
```

### Example
```excel
=EOMONTH(C2, D2)
```

| Argument | Description |
|----------|-------------|
| `C2` | Project start date |
| `D2` | Number of months to move forward/backward |
| Output | Returns the last day of the resulting month |

> 💡 Use `0` as months to get the last day of the **current month**.
> Use `-1` to get the last day of the **previous month**.

###  Use Cases
- Project deadline planning
- Financial period calculations
- Billing cycle management

---

## 7. NETWORKDAYS.INTL (Working Days)

###  Purpose
To calculate the number of **working days between two dates**, excluding custom weekends and holidays.

### Syntax
```excel
=NETWORKDAYS.INTL(start_date, end_date, weekend, holidays)
```

### Example
```excel
=NETWORKDAYS.INTL(A5, A35, 1, J$3:J$4)
```

### Weekend Codes

| Code | Weekend Days |
|------|-------------|
| `1` | Saturday & Sunday (default) |
| `2` | Sunday & Monday |
| `7` | Friday & Saturday |
| `11` | Sunday only |

### Arguments Explained

| Argument | Description |
|----------|-------------|
| `A5` | Start date |
| `A35` | End date |
| `1` | Weekend = Saturday & Sunday |
| `J$3:J$4` | Holiday list range |

###  Use Cases
- Payroll processing
- SLA (Service Level Agreement) tracking
- Working day analysis for projects

---

##  Quick Revision Table

| Function | Purpose | Syntax |
|----------|---------|--------|
| `DATE` | Build a date from Year, Month, Day | `=DATE(year, month, day)` |
| `Date Subtraction` | Number of days between dates | `=End_Date - Start_Date` |
| `DATEDIF("Y")` | Age / tenure in completed years | `=DATEDIF(start, end, "Y")` |
| `DATEDIF (Y,M,D)` | Exact age in Years + Months + Days | Combined DATEDIF formula |
| `TEXT` | Convert date to formatted text | `=TEXT(value, "format")` |
| `EOMONTH` | Last date of a month | `=EOMONTH(start_date, months)` |
| `NETWORKDAYS.INTL` | Count working days (excl. weekends & holidays) | `=NETWORKDAYS.INTL(start, end, weekend, holidays)` |

---

## Common Mistakes to Avoid

- ❌ Using `DATEDIF` without **quotes** around the unit code (e.g., `"Y"`, `"YM"`, `"MD"`)
- ❌ Forgetting `TODAY()` for **dynamic age** calculations — hardcoding today's date breaks the formula over time
- ❌ Using the **wrong weekend code** in `NETWORKDAYS.INTL`
- ❌ Treating a **text-formatted date** as a real Excel date — always validate with `ISNUMBER()`

---

>  *These Notes have been prepared during self-study | Excel for Data Analytics | Sanchal Kumar - Data Analyst*
