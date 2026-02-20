# Study of Pandas Library

Name: Bhomik Keshi
PRN: 25070123172
Experiment Number: 10

---

## Aim of the Experiment
The aim of this experiment is to study the Pandas library in Python and learn how to:
- Create and manipulate Series and DataFrames
- Perform basic data analysis
- Add, update, and delete columns
- Perform simple statistical analysis and filtering

---

## Introduction to Pandas Library
Pandas stands for "Panel Data".
It is a popular Python library used for handling structured data.
Pandas is useful for:
1. Working with structured data (like tables)
2. Exploratory Data Analysis (EDA)
3. Data cleaning and preprocessing
4. Data manipulation and transformation

---

## Experiment / Concept Procedure

### 1. Creating a Pandas Series
# Demonstration: creating a simple series

```bash
import pandas as pd

s = pd.Series([10, 20, 30, 40])
display(s)
```

# This shows a single column of data with an index.

---

### 2. Creating a DataFrame
# Demonstration: creating a simple DataFrame

```bash
data = {
    "Name": ["a", "b", "c"],
    "Marks": [85, 90, 78]
}
df = pd.DataFrame(data)
display(df)
```
# This creates a structured table with rows and columns.

---

### 3. Understanding the DataFrame
```bash
print(df.shape)    # Shape of DataFrame (Rows, Columns)
print(df.dtypes)   # Data type of each column
```
### 4. Accessing Data
```bash
display(df["Name"])  # Access the 'Name' column
display(df.loc[1])   # Access row with index 1
```

### 5. Previewing Data
```bash
display(df.head())  # First 5 rows
display(df.tail())  # Last 5 rows
```

### 6. Adding a New Column (Grade)
```bash
def assign_grade(marks):
    if marks >= 90:
        return "Distinction"
    elif marks >= 80:
        return "First Class"
    else:
        return "Second Class"

df["Grade"] = df["Marks"].apply(assign_grade)
display(df)
```

### 7. Updating Data
```bash
df.loc[0, "Marks"] = 81
display(df)
```

### 8. Deleting a Column
```bash
df.drop("Grade", axis=1, inplace=True, errors='ignore')
display(df)
```

### 9. Basic Statistical Analysis
```bash
mean_marks = df["Marks"].mean()
print()
min_marks = df["Marks"].min()
print()
max_marks = df["Marks"].max()
print()


display(mean_marks)
display(min_marks)
display(max_marks)
```

### 10. Filtering Data
```bash
display(df[df["Marks"] > 80])
```

---

## Observation
- Pandas allows easy creation and manipulation of structured data.
- Adding, updating, deleting, and filtering data is simple.
- Basic statistical analysis is built-in with functions like mean(), min(), max().

---

## Conclusion
- Pandas is a powerful library for data analysis in Python.
- It helps in handling tabular data efficiently.
- This experiment helped in understanding Series, DataFrames, and basic data operations.

---

## Author
Bhomik Keshi
PRN: 25070123172
