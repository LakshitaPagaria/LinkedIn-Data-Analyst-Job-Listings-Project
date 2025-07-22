# Global Data Analyst Job Market Analysis on LinkedIn

## Project Overview

This project performs a comprehensive analysis of the Data Analyst job market by examining over 8,400 job postings from LinkedIn across the USA, Canada, and Africa. The goal is to uncover key trends, identify in-demand skills, and understand the characteristics of available positions.

The entire data-to-insight pipeline is covered, starting from raw data collection, moving through cleaning and analysis in a Python Jupyter Notebook, and culminating in a fully interactive and dynamic dashboard built in Power BI. This project is designed to showcase a strong understanding of data analysis, feature engineering, and data storytelling.

---

## 📊 Power BI Dashboard Preview

Here is a preview of the interactive dashboard created to visualize the key findings of this analysis. The dashboard allows for dynamic filtering by region, seniority level, and work model to provide granular insights.

![LinkedIn Data Analyst Job Listings Dashboard](https://github.com/LakshitaPagaria/LinkedIn-Data-Analyst-Job-Listings-Project/blob/main/Linkedin%20Data%20Analyst%20Job%20Listings%20Dashboard.png)

---

## ❓ Key Questions Answered

This analysis seeks to answer the following critical questions for aspiring data professionals:
1.  Which regions (USA, Canada, Africa) have the most job opportunities for Data Analysts?
2.  What is the distribution of work models (On-site, Hybrid, Remote) across these regions?
3.  What is the typical salary range for Data Analysts, particularly in the USA?
4.  Which industries are the top recruiters for Data Analyst roles?
5.  What are the most frequently mentioned and in-demand technical skills in job descriptions?

---

## 💾 Data Source

The dataset used for this analysis was sourced from Kaggle and consists of three separate CSV files for different regions.

* **Dataset:** [LinkedIn Data Analyst Jobs Listings (USA, Canada, Africa)](https://www.kaggle.com/datasets/cedricaubin/linkedin-data-analyst-jobs-listings)

---

## ⚙️ Methodology

### 1. Data Collection & Merging
* Three distinct datasets (`linkedin-jobs-usa.csv`, `linkedin-jobs-canada.csv`, `linkedin-jobs-africa.csv`) were loaded into a Pandas DataFrame.
* A `country` column was added to each dataset before merging them into a single, unified DataFrame of 8,490 job listings.

### 2. Data Cleaning & Feature Engineering
This was a critical step to transform raw, messy data into a structured format suitable for analysis.
* **Criteria Parsing:** The `criteria` column, which was a string representation of a list of dictionaries, was parsed using Python's `ast` library. This extracted key features like `seniority_level`, `employment_type`, `job_function`, and `industries` into their own columns.
* **Salary Cleaning:** The `salary` column contained text and ranges (e.g., "$80,000 - $100,000"). A function was created to extract numerical values, handle ranges by taking the average, and create a new `average_salary` column.
* **Skill Extraction:** The `description` column was mined for mentions of key technical skills (e.g., SQL, Python, R, Excel, Tableau, Power BI, AWS). Boolean columns (`mentions_sql`, etc.) were created to flag the presence of each skill in a posting.
* **Standardization:** The `onsite_remote` column was standardized into a `work_model` column with capitalized, consistent values.

### 3. Exploratory Data Analysis (EDA)
Using the cleaned dataset, an in-depth EDA was conducted in the Jupyter Notebook (`linkedin_data_analyst_job_listings_analysis.ipynb`) to uncover initial trends and patterns. Visualizations were created using Matplotlib and Seaborn to illustrate the findings.

### 4. Data Visualization & Dashboarding
The final, cleaned dataset (`cleaned_global_linkedin_jobs.csv`) was exported and used as the source for an interactive dashboard in Power BI. The dashboard was designed with a professional blue and grey theme and includes:
* **KPI Cards:** Highlighting total jobs, total companies, and average salary.
* **Interactive Slicers:** For filtering the entire dashboard by Country, Seniority Level, and Work Model.
* **Visualizations:** Including a map for geographic distribution, bar charts for top industries and skills, and a donut chart for seniority breakdown.

---

## 🛠️ Tools & Technologies

* **Data Analysis:** Python, Pandas, Jupyter Notebook
* **Data Visualization:** Matplotlib, Seaborn, Power BI
* **Libraries Used:** `re` (for regular expressions), `ast` (for parsing string literals)

---

## 📈 Key Insights & Findings

### Job Distribution by Region
The analysis revealed that the **USA** has a significantly higher volume of Data Analyst job postings compared to Canada and Africa in this dataset, indicating a larger and more mature market.

### Prevalence of Work Models
**Hybrid** work is the most common model offered across all three regions, followed closely by fully **On-site** roles. Fully **Remote** positions are the least common, suggesting that while flexibility is increasing, a physical presence is still often preferred.

### Salary Insights (USA)
Salary data was most robust for the USA. As expected, there is a clear positive correlation between `seniority_level` and `average_salary`. Director and Executive roles command significantly higher compensation, while Entry-level and Associate roles form the lower end of the spectrum.

### Top Hiring Industries
The **IT Services & Consulting** and **Technology, Information & Media** sectors are the dominant industries hiring Data Analysts. This is followed by **Financial Services**, highlighting the data-centric nature of these fields.

### Most In-Demand Skills
**SQL** and **Excel** remain the most fundamental and frequently requested skills. Following closely are **Python**, **Tableau**, and **Power BI**, underscoring the need for a blend of database, programming, and visualization capabilities.

---

## 🚀 How to Use This Repository

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
    ```
2.  **Install the required libraries:**
    ```bash
    pip install pandas matplotlib seaborn jupyter
    ```
3.  **Run the Jupyter Notebook:**
    Open `linkedin_data_analyst_job_listings_analysis.ipynb` in Jupyter Notebook to view the full data cleaning and analysis process.
4.  **View the Dashboard:**
    The `Linkedin Data Analyst Job Listings Dashboard.jpg` file provides a static view of the final dashboard.

---

## 🏁 Conclusion

This project provides a detailed snapshot of the global Data Analyst job market, offering valuable insights for job seekers. It demonstrates an end-to-end analytical workflow, from handling complex, unstructured data to presenting findings in a clear and compelling interactive dashboard. The key takeaway is that a strong foundation in SQL and Excel, complemented by proficiency in Python and a major BI tool like Power BI or Tableau, is crucial for success in this field.
