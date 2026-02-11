# 🔢 Chapter 4 – Logical Functions & Conditional Analysis (Excel)

This chapter focuses on using logical functions in Excel to make decisions based on conditions.
Logical functions are heavily used in real-world analytics for eligibility checks, grading systems,
bonus calculations, and automated business rules.

---

##  Goal of This Chapter

- Apply conditional logic using IF
- Handle multiple conditions using Nested IF and IFS
- Combine conditions using AND / OR
- Build grading and incentive systems
- Automate decision-making in Excel

---

##  Topics Covered

---

### 1. IF Function (Basics)

Used to return different values based on a condition.

Syntax:

```excel
=IF(condition, value_if_true, value_if_false)
```

Example:

```excel
=IF(A2>=40,"Pass","Fail")
```

Use cases:

- Pass / Fail
- Salary status
- Eligibility check

---

### 2. Nested IF

Used when multiple conditions are required.

Example:

```excel
=IF(A2>=80,"A",IF(A2>=60,"B",IF(A2>=40,"C","Fail")))
```

Use cases:

- Grade systems
- Performance levels
- Bonus slabs

---

### 3. AND Function

Returns TRUE only when all conditions are true.

Syntax:

```excel
=AND(condition1, condition2)
```

Example:

```excel
=IF(AND(A2>=60,B2="Yes"),"Eligible","Not Eligible")
```

Used for:

- Multiple eligibility checks
- Attendance + marks validation

---

### 4. OR Function

Returns TRUE when any one condition is true.

Syntax:

```excel
=OR(condition1, condition2)
```

Example:

```excel
=IF(OR(A2>=60,B2="Yes"),"Approved","Rejected")
```

Used for:

- Alternative conditions
- Approval logic

---

### 5. IFS Function

Modern replacement of Nested IF.

Example:

```excel
=IFS(A2>=80,"A",A2>=60,"B",A2>=40,"C",TRUE,"Fail")
```

Advantages:

- Cleaner syntax
- Easier to read
- No deep nesting

---

# Practical Use Cases

- Student grading systems
- Employee bonus calculation
- Eligibility validation
- Automated decision tables
- Business rule implementation

---

# Outcome

After completing this chapter, I can:

- Write IF based logic
- Handle multiple conditions
- Build grading systems
- Automate decisions in Excel
- Apply AND / OR conditions professionally

These skills are essential for Data Analyst roles.


---

👤 Author  
**Sanchal Kumar**  
(Data Analytics – Excel Learning Journey)
