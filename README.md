# Excel-data-cleaning

# 📊 SaaS Sales Data Cleaning Project (Excel)

## 📌 Project Overview

This project focuses on cleaning and formatting a SaaS sales dataset using Microsoft Excel.

The objective was not just to clean the dataset technically, but to understand the **business logic behind each column** and ensure that cleaning decisions did not negatively impact financial analysis.

---

## 📂 Files in This Repository

- `Raw_Dataset.xlsx` → Original dataset  
- `Cleaned_Dataset.xlsx` → Cleaned and formatted dataset  

---

## 🧠 Step 1: Business Understanding

Before starting the cleaning process, I analyzed:

- What each column represents  
- Expected data types and formats  
- Possible derived metrics  

Examples:
- Revenue & Profit → Currency ($)
- Profit Margin → Percentage (%)
- Date → Date format

Understanding this helped avoid incorrect formatting or accidental data loss.

---

## 🧹 Data Cleaning Steps Performed

### 1️⃣ Date Formatting
- Converted values into proper Date format.

---

### 2️⃣ Client Column Cleaning

Original format:
AMAZON.COM, INC. (XNAS:AMZN)

Action:
- Used **Text to Columns**
- Delimiter: "("
- Removed stock exchange information inside parentheses

Result:
Clean client names without unnecessary metadata.

---

### 3️⃣ Contact Column Cleaning

Issues identified:
- Leading/trailing spaces
- Inconsistent capitalization

Formula used:

=PROPER(TRIM(D3))

- `TRIM()` → Removes extra spaces  
- `PROPER()` → Converts text to proper case  

Example:
Bill SmITH → Bill Smith

---

### 4️⃣ Department Column Splitting

Original format:
Cloud Tech_Texas

Action:
- Used **Text to Columns**
- Delimiter: "_"

Split into:
- Department Name
- State

Improved structure and readability.

---

### 5️⃣ Revenue & Profit Formatting
- Converted to Currency format ($)
- Ensured numeric consistency

---

### 6️⃣ Profit Margin Formatting
- Formatted as Percentage (%)
- Ensured calculation consistency

---

### 7️⃣ Handling Missing Values
- Identified empty cells
- Replaced blanks with "NA" where appropriate

---

## ⚠️ Key Learning Moment

I initially deleted 2 rows where Revenue was missing but Profit had values.

After reviewing and seeking feedback, I realized:

- Deleting those rows could significantly impact total profit.
- Data cleaning decisions directly affect financial outcomes.

### Lesson Learned:

> Data cleaning is not just technical. It has business and financial impact.

From now on, I will:
- Validate business logic before deleting rows
- Consider financial impact
- Document decisions clearly

---

## 🛠 Tools & Techniques Used

- Microsoft Excel  
- Text to Columns (Delimiters: "(" and "_")  
- TRIM()  
- PROPER()  
- Data Formatting (Date, Currency, Percentage)  
- Missing value handling  
- Business logic validation  

---

## 🚀 Key Takeaways

- Always start with business understanding.
- Never delete financial data without impact analysis.
- Cleaning is about preserving business truth, not just formatting cells.
- AI tools can assist in validation, but critical thinking is essential.

---

## 📈 Next Steps

- Practice more real-world datasets  
- Apply similar cleaning techniques using Python (Pandas)  
- Improve documentation and reproducibility  

---

## 👩‍💻 Author

**Aishwarya**  
Aspiring Data Analyst | Learning by Doing | Focused on Business-Driven Data Thinking  
