

# 🏥 Healthcare Data Visualization & Correlation Analysis (R)

This project performs **exploratory data analysis (EDA)** on a healthcare dataset using **R**. It visualizes relationships between key health indicators and computes their correlation matrix.

---

## 📌 Project Information

* **Student Name:** Prithivi Raj
* **Roll No:** 23BAD088
* **Language:** R
* **Libraries Used:** `ggplot2`, `dplyr`, `GGally`

---

## 📊 Dataset Description

The dataset (`3.healthcare_data.csv`) contains patient health information, including:

* **Age** – Patient age
* **BMI** – Body Mass Index
* **Glucose_Level** – Blood glucose level
* **Blood_Pressure** – Blood pressure readings

An additional variable, **Age_Group**, is created based on age:

| Age Range | Group       |
| --------- | ----------- |
| 0–30      | Young       |
| 31–50     | Middle-aged |
| 51+       | Senior      |

---

## ⚙️ Features of the Code

### 1. Data Loading

Reads the healthcare dataset from a local CSV file.

```r
patient_data <- read.csv("3.healthcare_data.csv")
```

---

### 2. Age Group Classification

Patients are categorized into age groups for better visualization.

```r
patient_data$Age_Group <- cut(
  patient_data$Age,
  breaks = c(0, 30, 50, 100),
  labels = c("Young", "Middle-aged", "Senior")
)
```

---

### 3. Scatter Plot Matrix

A **scatter plot matrix** is generated using `ggpairs()` to visualize relationships between:

* Age
* BMI
* Glucose Level
* Blood Pressure

Plots are color-coded by **Age Group**.

---

### 4. Correlation Analysis

Computes and prints the **correlation matrix** for the selected health indicators.

```r
cor_matrix <- cor(health_vars)
```

---

## 📈 Output

* **Scatter Plot Matrix** showing pairwise relationships
* **Correlation Matrix** with rounded correlation values
* Custom plot title including student name and roll number

---

## 🛠️ Required Libraries

Install required packages before running the script:

```r
install.packages("ggplot2")
install.packages("dplyr")
install.packages("GGally")
```

---

## ▶️ How to Run

1. Clone this repository
2. Place `3.healthcare_data.csv` in the working directory
3. Open the R script in **RStudio**
4. Run the script

---

## 📌 Notes

* Ensure column names in the dataset match:

  * `Age`
  * `BMI`
  * `Glucose_Level`
  * `Blood_Pressure`
* Update the file path if your dataset is stored elsewhere

---

