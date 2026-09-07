# 🤖 AI Impact on Jobs & Salaries — Data Analysis

A comprehensive data analysis project that explores how Artificial Intelligence is affecting jobs, employment trends, required skills, and salaries across the global tech landscape[cite: 2]. The project leverages Python, Pandas, NumPy, Matplotlib, Seaborn, and SciPy to extract actionable insights from **71,913 verified job-market records** spanning 2020 to 2025 across 97 countries.

![AI Jobs & Salaries Summary Dashboard]
<img width="2430" height="1380" alt="00_summary_dashboard" src="https://github.com/user-attachments/assets/ab4f68ef-7987-4cde-be97-b8d6729d62a1" />


---

## 📌 Project Overview
Artificial Intelligence is rapidly transforming the global labor market[cite: 2]. While routine technical workflows are increasingly automated, demand for specialized AI architects, machine learning engineers, and scalable data infrastructure has surged[cite: 1, 2]. 

This project analyzes empirical compensation and hiring data to understand:
* **Hiring Volume & AI Adoption:** The velocity of job openings between 2020 and 2025[cite: 1, 2].
* **Salary Benchmarks:** Distribution of base pay, median earnings, and market peaks[cite: 1, 2].
* **Seniority Premiums:** Income trajectory across Entry, Mid, Senior, and Executive tiers[cite: 1, 2].
* **Role Specialization:** Compensation differences between AI/ML specialists and traditional data roles[cite: 1, 2].
* **Workplace Flexibility:** Earning power across Remote, On-site, and Hybrid work models[cite: 1, 2].
* **Geographical & Organizational Scale:** Where hiring is concentrated and how company size impacts pay[cite: 1, 2].

---

## 🎯 Objectives
* Conduct comprehensive Exploratory Data Analysis (EDA) on global career datasets[cite: 2].
* Preprocess and clean data by addressing missing values and validating duplicates[cite: 1, 2].
* Identify and filter statistical salary outliers using Interquartile Range (IQR) fencing[cite: 1, 2].
* Track Year-over-Year (YoY) salary shifts and market normalization phases[cite: 2].
* Build high-contrast, publication-quality visualizations[cite: 2].
* Formulate data-driven conclusions for researchers, engineers, and hiring managers[cite: 2].

---

## 🛠️ Technologies Used
* **Python** — Core analysis runtime
* **Pandas** — Data manipulation, aggregation, and cleansing
* **NumPy** — Vectorized numerical operations[cite: 1]
* **Matplotlib** — Custom visualization architecture and plot rendering[cite: 1]
* **Seaborn** — Statistical distributions, violin plots, and correlation heatmaps[cite: 1]
* **SciPy** — Distributional statistics (skewness, kurtosis)[cite: 1]
* **Jupyter Notebook** — Interactive code execution and narrative documentation[cite: 1]

---

## 🔍 Analysis Performed

### 1. Data Cleaning & Integrity Check
* **Duplicate Rows:** Verified 0 duplicate records across the entire dataset[cite: 1, 2].
* **Missing Values:** Only `isco_group_hint` contained missing entries (40,540 rows; 56.37%)[cite: 1, 2]. All remaining 16 attributes possess 100% completeness[cite: 1, 2].

![Missing Values by Column](figures/01_missing_values.png)
<img width="1479" height="737" alt="01_missing_values" src="https://github.com/user-attachments/assets/2a36bde3-65cf-4960-95bc-c6add399fc99" />


* **Outlier Analysis:** Nominal salary data has a positive skewness of 1.48 and kurtosis of 5.12, with salaries scaling up to $800,000[cite: 1, 2]. Filtering using 1.5×IQR boundaries isolated 1,754 outlier records (2.44%), yielding a clean baseline of 70,159 records with a median of $136,700[cite: 1, 2].

![Salary Distribution — With vs. Without Outliers](figures/02_salary_distribution.png)
<img width="2085" height="745" alt="02_salary_distribution" src="https://github.com/user-attachments/assets/60dbad6d-7949-4534-90c4-1704608161c7" />


---

### 2. Hiring Volume & Year-over-Year (YoY) Salary Trends
* **Recruitment Explosion:** Annual record counts expanded 510x from 75 in 2020 to 38,282 in 2025[cite: 1, 2]. The 2024–2025 period represents 91.7% of all sampled hiring data[cite: 1, 2].

![Number of Job Records per Year](figures/03_records_per_year.png)
<img width="1485" height="737" alt="03_records_per_year" src="https://github.com/user-attachments/assets/3813af22-c79b-4f49-b7ae-12dfe9a5bda8" />


* **Compensation Trajectory:** Median compensation rose sharply from $80,000 in 2020 to a peak of $141,000 in 2023, then stabilized at $138,000 (2024) and $136,000 (2025) as talent supply caught up with enterprise demand[cite: 2].

![Salary Trend & Volume Growth (2020-2025)](figures/05_salary_trend_over_time.png)
<img width="1786" height="887" alt="05_salary_trend_over_time" src="https://github.com/user-attachments/assets/17503015-27a2-4e86-8acc-8faa84af2634" />



* **YoY Growth Analysis:**
  * **2021:** +3.4% YoY median growth ($83,000)[cite: 2].
  * **2022:** +56.3% YoY median growth ($129,000) during peak model deployment initiatives[cite: 2].
  * **2023:** +9.3% YoY median growth ($141,000)[cite: 2].
  * **2024:** -2.4% YoY market calibration ($138,000)[cite: 2].
  * **2025:** -1.3% YoY market stabilization ($136,000)[cite: 2].

![Salary Growth Analysis — Year-over-Year](figures/24_yoy_salary_growth.png)
<img width="2085" height="745" alt="24_yoy_salary_growth" src="https://github.com/user-attachments/assets/aa70b8eb-be9e-4c7f-9a21-8f3f1f46e436" />


---

### 3. Workforce Demographics & Categorical Breakdown
* **Seniority:** Senior-level (52.4%), Mid-level (32.5%), Entry-level (11.1%), Executive-level (4.0%)[cite: 1, 2].
* **Employment Type:** Full-time roles represent 99.0% of the sample, with contract, part-time, and freelance making up 1.0%[cite: 1, 2].
* **Work Mode:** On-site roles represent 75.2%, Remote roles make up 24.3%, and Hybrid roles represent 0.5%[cite: 1, 2].
* **Company Size:** Medium-sized firms (50–250 employees) drive 97.5% of market volume[cite: 1, 2].

![Categorical Feature Distributions](figures/04_categorical_distributions.png)
<img width="1645" height="1477" alt="04_categorical_distributions" src="https://github.com/user-attachments/assets/724c8b76-1fd2-4e94-9969-c8871f69fa3c" />


---

### 4. Experience vs. Salary
Compensation scales directly with experience level[cite: 2]:
* **Entry-level (`EN`):** Median of **$85,000** (IQR: $60K – $122K; n=7,975)[cite: 2].
* **Mid-level (`MI`):** Median of **$120,000** (IQR: $85K – $166K; n=23,395) → **+41.2%** over Entry[cite: 2].
* **Senior-level (`SE`):** Median of **$154,000** (IQR: $115K – $201K; n=37,702) → **+81.2%** over Entry[cite: 2].
* **Executive-level (`EX`):** Median of **$184,000** (IQR: $142K – $233K; n=2,841) → **2.16x** the Entry-level benchmark[cite: 2].

![Salary Distribution by Experience Level](figures/07_salary_by_experience.png)
<img width="2235" height="892" alt="07_salary_by_experience" src="https://github.com/user-attachments/assets/34159881-4289-454a-8d04-c8c2ddbd65cc" />


---

### 5. Role Families & Hiring Specialization
Hiring for specialized AI and engineering roles increased substantially alongside traditional data teams[cite: 1, 2]:

![Top Role Families — Record Count Growth](figures/06_role_family_growth.png)
<img width="1935" height="887" alt="06_role_family_growth" src="https://github.com/user-attachments/assets/c64e9536-4aa3-404d-98ed-c27e4e4c06aa" />


System architecture and machine learning research roles command the highest median salaries[cite: 2]:
1. **AI Architect:** **$185,000** (n=199)[cite: 1, 2]
2. **Research Scientist:** **$173,000** (n=2,642)[cite: 1, 2]
3. **Machine Learning Engineer:** **$171,000** (n=3,460)[cite: 1, 2]
4. **Computer Vision Engineer:** **$170,000** (n=134)[cite: 1, 2]
5. **Analytics Manager:** **$161,000** (n=459)[cite: 1, 2]
6. **NLP Engineer:** **$150,000** (n=19)[cite: 1, 2]
7. **AI Engineer:** **$148,000** (n=1,165)[cite: 1, 2]
8. **Data Scientist:** **$140,000** (n=7,102)[cite: 1, 2]
9. **Data Engineer:** **$135,000** (n=7,168)[cite: 1, 2]
10. **Data Analyst:** **$99,000** (n=8,313)[cite: 1, 2]

![Median Salary by Role Family](figures/08_salary_by_role_family.png)
<img width="1934" height="1037" alt="08_salary_by_role_family" src="https://github.com/user-attachments/assets/38b20b42-b00d-4f24-a135-398bf6bd0861" />


---

### 6. Top 20 Highest-Paying Job Titles
Examining designations with at least 20 records shows product leadership and specialized AI infrastructure roles leading the market[cite: 2]:

![Top 20 Highest-Paying AI Job Titles](figures/09_top20_job_titles.png)
<img width="1934" height="1186" alt="09_top20_job_titles" src="https://github.com/user-attachments/assets/56d509e7-2a2a-43f2-a740-3e8b07e7c199" />


* **Director of Product Management:** **$250,000**[cite: 2]
* **Head of AI:** **$230,000**[cite: 2]
* **Engineering Manager:** **$220,000**[cite: 2]
* **Director of Machine Learning:** **$208,000**[cite: 2]
* **AI Product Manager:** **$204,000**[cite: 2]
* **Head of Data:** **$196,000**[cite: 1, 2]
* **Director:** **$191,000**[cite: 2]
* **Tech Lead:** **$190,000**[cite: 2]
* **Software Architect:** **$187,000**[cite: 2]
* **Economist:** **$185,000**[cite: 2]

---

### 7. Work Modality & Company Size Impact
* **Work Mode:** Remote roles maintain slight compensation parity with on-site roles, while hybrid roles show a 50% discount due to lower seniority representations[cite: 2].
  * **Remote:** Median of **$140,000** (24.3% market share)[cite: 1, 2].
  * **On-site:** Median of **$136,000** (75.2% market share)[cite: 1, 2].
  * **Hybrid:** Median of **$68,000** (0.5% market share)[cite: 1, 2].

![Salary by Work Mode](figures/10_salary_by_work_mode.png)
<img width="2085" height="892" alt="10_salary_by_work_mode" src="https://github.com/user-attachments/assets/c56478a2-5ca1-41bd-b7bc-398b41f8b0e8" />


* **Company Size:** Mid-sized firms lead overall median base pay, whereas small organizations offer lower baseline cash[cite: 2].
  * **Medium (50–250 staff):** Median of **$137,000** (97.5% volume share)[cite: 1, 2].
  * **Large (>250 staff):** Median of **$129,000** (2.2% volume share)[cite: 1, 2].
  * **Small (<50 staff):** Median of **$75,000** (0.3% volume share)[cite: 1, 2].

![Salary Distribution by Company Size](figures/11_salary_by_company_size.png)
<img width="1635" height="887" alt="11_salary_by_company_size" src="https://github.com/user-attachments/assets/c1158e4e-d7a2-4108-a449-6b85bde7d795" />


---

### 8. Geographic Distribution
The United States accounts for 83.6% (60,147 positions) of total hiring volume, followed by Canada (4,571) and the United Kingdom (2,835)[cite: 1, 2].

![Top 15 Company Locations by Job Count](figures/12_top_company_locations.png)
<img width="1775" height="1037" alt="12_top_company_locations" src="https://github.com/user-attachments/assets/460133cd-d685-49bd-98af-b0b65ff3ead2" />


---

### 9. Feature Correlations
Pearson correlation coefficients reveal minimal linear coupling among numeric parameters[cite: 2]:
* **`work_year` vs. `salary_in_usd` ($r = 0.018$):** Early wage surges normalized in 2024–2025 as mid/junior hiring expanded[cite: 2].
* **`work_year` vs. `remote_ratio` ($r = -0.100$):** Captures gradual post-pandemic return-to-office adjustments[cite: 2].
* **`salary_in_usd` vs. `remote_ratio` ($r = 0.002$):** Confirms salary is driven by technical specialty and seniority rather than remote location[cite: 2].

![Correlation Matrix — Numerical Features](figures/23_correlation_matrix.png)
<img width="986" height="736" alt="23_correlation_matrix" src="https://github.com/user-attachments/assets/908af60f-ab7e-4740-a69a-ad49d6a8aef6" />

---

## 📊 Key Questions Answered
* **Which roles pay the most?** Product management directors, Heads of AI, and AI Architects earn the highest median salaries, reaching between $185,000 and $250,000[cite: 2].
* **Does AI specialization command a premium?** Yes, AI Architects earn an **86.8% premium** over general Data Analysts ($185K vs. $99K)[cite: 2].
* **How much does experience impact salary?** Senior roles command an 81.2% premium over entry-level workers, while executives earn more than double[cite: 2].
* **Are remote jobs paid less?** No, fully remote professionals report a median salary of $140,000, slightly above on-site peers ($136,000)[cite: 2].
* **How has hiring volume changed?** Total records grew 510x from 2020 to 2025, driven by enterprise AI adoption[cite: 1, 2].

---

## 📁 Project Structure

```text
AI-Impact-on-Jobs-and-Salaries/
│
├── DATASET/
│   └── ai_jobs_salaries_clean.csv       # Standardized dataset (71,913 records)
│
├── figures/
│   ├── 00_summary_dashboard.png         # High-level metric dashboard
│   ├── 01_missing_values.png            # Feature missingness audit
│   ├── 02_salary_distribution.png       # Raw vs. cleaned salary distributions
│   ├── 03_records_per_year.png          # Yearly hiring volume growth
│   ├── 04_categorical_distributions.png # Categorical composition breakdown
│   ├── 05_salary_trend_over_time.png    # 2020–2025 salary evolution vs. volume
│   ├── 06_role_family_growth.png        # Headcount expansion across role families
│   ├── 07_salary_by_experience.png      # Seniority box plots and KDE distributions
│   ├── 08_salary_by_role_family.png     # Median salary & IQR by role family
│   ├── 09_top20_job_titles.png          # Top 20 highest-paying job titles
│   ├── 10_salary_by_work_mode.png       # Work mode violin and bar comparison
│   ├── 11_salary_by_company_size.png    # Company size comparison box plot
│   ├── 12_top_company_locations.png     # Top 15 hiring countries by volume
│   ├── 23_correlation_matrix.png        # Correlation heatmap of numeric variables
│   └── 24_yoy_salary_growth.png         # Year-over-year median salary growth rates
│
├── code.ipynb                           # Data analysis notebook
├── README.md                            # Project documentation
└── requirements.txt                     # Python dependencies
```

🚀 Getting Started

1. Clone the Repository

git clone [https://github.com/Subrat-ku-sahoo19/AI-Impact-on-Jobs-and-Salaries.git](https://github.com/Subrat-ku-sahoo19/AI-Impact-on-Jobs-and-Salaries.git)

cd AI-Impact-on-Jobs-and-Salaries



2. Install Dependencies

pip install -r requirements.txt



3. Run the Notebook

jupyter notebook code.ipynb



📦 Requirements

pandas

numpy

matplotlib

seaborn

scipy

jupyter





👨‍💻 Author

Subrat Kumar Sahoo



B.Tech — Computer Science & Engineering



GitHub: @Subrat-ku-sahoo19



⭐ If you found this analysis useful, consider giving the repository a star!

