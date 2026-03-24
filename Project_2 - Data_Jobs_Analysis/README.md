# Project 2 – Data Jobs Analysis

## 📌 Overview

As someone who has actively explored opportunities in the data field, I noticed a gap in structured insights around job trends, required skills, and salary benchmarks. This project aims to bridge that gap by analyzing real-world data to understand what drives higher-paying roles in the data industry.

---

## ❓ Key Questions Explored

To gain clarity on the data job landscape, I focused on the following:

1. **Does having more skills lead to higher salaries?**
2. **How do salaries vary across different regions?**
3. **Which skills are most in-demand among data professionals?**
4. **What is the salary impact of the top skills?**

---

## 🛠️ Tools \& Techniques Used

This analysis was carried out using the following Excel capabilities:

* **Pivot Tables**
* **Pivot Charts**
* **DAX (Data Analysis Expressions)**
* **Power Query (ETL)**
* **Power Pivot (Data Modeling)**

---

## 📂 Dataset Information

The dataset used in this project contains job-related data from 2023 till December 2025, including roles within the data domain. It was sourced as part of a structured Excel learning program.

### Data includes:

* Job Titles
* Salary Information
* Geographic Locations
* Required Skills

---

# 1️⃣ Do More Skills Lead to Better Pay?

## 🔍 Approach – Power Query (ETL Process)

### 📥 Data Extraction

* Imported the raw dataset (`data\_salary\_all.xlsx`) using Power Query
* Created two separate queries:

  * One for overall job data
  * One mapping job IDs to skills

---

### 🔄 Data Transformation

* Cleaned and standardized data:

  * Adjusted column data types
  * Removed unnecessary fields
  * Cleaned text values and extra spaces

📸 **Preview of transformed data:**

* Data Jobs Table:  
  <img width="244" height="312" alt="2_Project_Analysis_Screenshot1" src="https://github.com/user-attachments/assets/789d88e4-28af-4e8a-b424-f273375c011d" />

* Job Skills Table:  
  <img width="243" height="328" alt="2_Project_Analysis_Screenshot2" src="https://github.com/user-attachments/assets/026ace0e-3c4e-4468-b847-863bd220f890" />


---

### 🔗 Data Loading

* Loaded cleaned datasets into Excel for analysis

📸 **Loaded data views:**

* Loaded Jobs Data  
  <img width="1916" height="649" alt="2_Project_Analysis_Screenshot3" src="https://github.com/user-attachments/assets/703c275d-254b-40cd-b543-8bfa5e6c5e98" />

* Loaded Skills Data  
  <img width="1914" height="702" alt="2_Project_Analysis_Screenshot4" src="https://github.com/user-attachments/assets/99b11679-4e8d-44ef-87eb-8bacc3ef106e" />


---

## 📊 Findings

### 💡 Insights

* There is a noticeable trend where roles requiring a broader skill set tend to offer higher median salaries.
* Positions like **Senior Data Engineer** and **Data Scientist** show strong alignment between skill count and compensation.
* Roles with fewer technical requirements (e.g., Business Analyst) generally fall on the lower end of the salary spectrum.

📊 **Visualization:**

<img width="1333" height="622" alt="2_Project_Analysis_Chart1" src="https://github.com/user-attachments/assets/7bd00fb6-f06d-484c-aaaa-a64cc46a91fa" />

---

### 🤔 Key Takeaway

Building a diverse and relevant skill set can significantly improve earning potential in data-related careers.

---

# 2️⃣ Salary Comparison Across Regions

## 🧮 Approach – PivotTables \& DAX

### 📊 Pivot Table Setup

* Created a PivotTable using the Data Model
* Fields used:

  * Rows → `job_title_short`
  * Values → `salary_year_avg`

---

### 🧮 DAX Measures

**Median Salary (Overall):**  
Median Salary := MEDIAN(data\_jobs\_all\[salary\_year\_avg])



**Median Salary (United States):**

```
=CALCULATE(
MEDIAN(data\_jobs\_all\[salary\_year\_avg]),
data\_jobs\_all\[job\_country] = "United States"
)
```


---

## 📊 Findings

### 💡 Insights

* Senior-level roles consistently command higher salaries across regions.
* There is a clear salary gap between US and non-US roles, especially in technical positions.
* This difference may be influenced by industry concentration and demand in specific regions.

📊 **Visualization:**

<img width="1229" height="388" alt="2_Project_Analysis_Chart2" src="https://github.com/user-attachments/assets/3a17931d-31fd-4066-83b1-078f45c738d1" />

---

### 🤔 Key Takeaway

Geographical location plays a major role in salary expectations and should be considered when evaluating opportunities.

\---

# 3️⃣ Most In-Demand Skills in Data Roles

## 🔧 Approach – Power Pivot

### 🔗 Data Modeling

* Combined job and skill datasets into a unified data model
* Established relationships using `job\_id`

📸 **Data Model View:**

* <img width="1788" height="1264" alt="2_Project_Analysis_Screenshot5" src="https://github.com/user-attachments/assets/ded7bb96-38ca-4f70-bc49-fe236d706b0f" />

---

### ⚙️ Power Pivot Usage

* Used Power Pivot to:

  * Manage relationships
  * Create measures
  * Enable deeper analysis

📸 **Power Pivot Interface:**

* <img width="1918" height="742" alt="2_Project_Analysis_Screenshot6" src="https://github.com/user-attachments/assets/66956843-bdbc-44a2-9e50-792581c22cbe" />

---

## 📊 Findings

### 💡 Insights

* **SQL and Python** emerge as the most essential skills across roles.
* Cloud-related tools like **AWS** and **Azure** are increasingly in demand.
* The skill landscape indicates a shift toward scalable and cloud-based technologies.

📊 **Visualization:**

*<img width="913" height="522" alt="2_Project_Analysis_Chart3" src="https://github.com/user-attachments/assets/0e8cafdf-3552-44c8-ae47-50c522b244fd" />

---

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

* <img width="1037" height="563" alt="2_Project_Analysis_Chart4" src="https://github.com/user-attachments/assets/5e0e3ea1-8f58-412f-957a-43888a2ff9bf" />

---

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

