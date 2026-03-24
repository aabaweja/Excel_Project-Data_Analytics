# Project 2 – Data Jobs Analysis

## 📌 Overview

As someone who has actively explored opportunities in the data field, I noticed a gap in structured insights around job trends, required skills, and salary benchmarks. This project aims to bridge that gap by analyzing real-world data to understand what drives higher-paying roles in the data industry.

\---

## ❓ Key Questions Explored

To gain clarity on the data job landscape, I focused on the following:

1. **Does having more skills lead to higher salaries?**
2. **How do salaries vary across different regions?**
3. **Which skills are most in-demand among data professionals?**
4. **What is the salary impact of the top skills?**

\---

## 🛠️ Tools \& Techniques Used

This analysis was carried out using the following Excel capabilities:

* **Pivot Tables**
* **Pivot Charts**
* **DAX (Data Analysis Expressions)**
* **Power Query (ETL)**
* **Power Pivot (Data Modeling)**

\---

## 📂 Dataset Information

The dataset used in this project contains job-related data from 2023 till December 2025, including roles within the data domain. It was sourced as part of a structured Excel learning program.

### Data includes:

* Job Titles
* Salary Information
* Geographic Locations
* Required Skills

\---

# 1️⃣ Do More Skills Lead to Better Pay?

## 🔍 Approach – Power Query (ETL Process)

### 📥 Data Extraction

* Imported the raw dataset (`data\_salary\_all.xlsx`) using Power Query
* Created two separate queries:

  * One for overall job data
  * One mapping job IDs to skills

\---

### 🔄 Data Transformation

* Cleaned and standardized data:

  * Adjusted column data types
  * Removed unnecessary fields
  * Cleaned text values and extra spaces

📸 **Preview of transformed data:**

* \[Add Image – Data Jobs Table]
* \[Add Image – Job Skills Table]

\---

### 🔗 Data Loading

* Loaded cleaned datasets into Excel for analysis

📸 **Loaded data views:**

* \[Add Image – Loaded Jobs Data]
* \[Add Image – Loaded Skills Data]

\---

## 📊 Findings

### 💡 Insights

* There is a noticeable trend where roles requiring a broader skill set tend to offer higher median salaries.
* Positions like **Senior Data Engineer** and **Data Scientist** show strong alignment between skill count and compensation.
* Roles with fewer technical requirements (e.g., Business Analyst) generally fall on the lower end of the salary spectrum.

📊 **Visualization:**

* \[Insert Chart Image Here]

\---

### 🤔 Key Takeaway

Building a diverse and relevant skill set can significantly improve earning potential in data-related careers.

\---

# 2️⃣ Salary Comparison Across Regions

## 🧮 Approach – PivotTables \& DAX

### 📊 Pivot Table Setup

* Created a PivotTable using the Data Model
* Fields used:

  * Rows → `job\_title\_short`
  * Values → `salary\_year\_avg`

\---

### 🧮 DAX Measures

**Median Salary (Overall):**
Median Salary := MEDIAN(data\_jobs\_all\[salary\_year\_avg])



**Median Salary (United States):**

=CALCULATE(
MEDIAN(data\_jobs\_all\[salary\_year\_avg]),
data\_jobs\_all\[job\_country] = "United States"
)



\---

## 📊 Findings

### 💡 Insights

* Senior-level roles consistently command higher salaries across regions.
* There is a clear salary gap between US and non-US roles, especially in technical positions.
* This difference may be influenced by industry concentration and demand in specific regions.

📊 **Visualization:**

* \[Insert Chart Image Here]

\---

### 🤔 Key Takeaway

Geographical location plays a major role in salary expectations and should be considered when evaluating opportunities.

\---

# 3️⃣ Most In-Demand Skills in Data Roles

## 🔧 Approach – Power Pivot

### 🔗 Data Modeling

* Combined job and skill datasets into a unified data model
* Established relationships using `job\_id`

📸 **Data Model View:**

* \[Insert Data Model Image]

\---

### ⚙️ Power Pivot Usage

* Used Power Pivot to:

  * Manage relationships
  * Create measures
  * Enable deeper analysis

📸 **Power Pivot Interface:**

* \[Insert Screenshot Here]

\---

## 📊 Findings

### 💡 Insights

* **SQL and Python** emerge as the most essential skills across roles.
* Cloud-related tools like **AWS** and **Azure** are increasingly in demand.
* The skill landscape indicates a shift toward scalable and cloud-based technologies.

📊 **Visualization:**

* \[Insert Chart Image Here]

\---

### 🤔 Key Takeaway

Focusing on core technical skills along with cloud technologies can significantly boost employability in the data domain.

\---

# 4️⃣ Salary Impact of Top Skills

## 📊 Approach – Advanced Visualization (Pivot Charts)

### 📈 Chart Design

* Built a combination chart to compare:

  * Median Salary
  * Skill Demand (%)

**Chart Components:**

* Primary Axis → Median Salary (Column Chart)
* Secondary Axis → Skill Demand (Line Chart)

\---

## 📊 Findings

### 💡 Insights

* Skills such as **Python, SQL, and Oracle** are associated with higher salary ranges.
* Tools like **PowerPoint and Word** show lower salary impact, indicating lower specialization value.
* High-paying skills are typically technical and data-focused.

📊 **Visualization:**

* \[Insert Chart Image Here]

\---

### 🤔 Key Takeaway

Investing time in learning high-impact technical skills can directly influence earning potential.

\---

# 🧾 Conclusion

This project provided valuable insights into the data job market by analyzing real-world job data using Excel. Through the use of Power Query, PivotTables, DAX, and data modeling, key patterns were identified linking skills, roles, and salaries.

The analysis highlights:

* The importance of multi-skill proficiency
* The impact of geography on salaries
* The dominance of core technical skills like Python and SQL

Overall, this project serves as a practical reference for anyone looking to better understand the data job ecosystem and align their skill development with market demand.

\---

## 🔗 Additional Links

* 📊 **Project Dashboard:** \[Insert Dashboard Link Here]
* 💻 **GitHub Repository:** \[Insert Repo Link Here]
* 📷 **Project Screenshots:** \[Insert Image Folder Link Here]

