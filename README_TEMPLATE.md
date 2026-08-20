# Data Professional Survey Analysis
> *Exploring Roles, Salaries, Skills, Demographics, and Job Satisfaction with Power Bi*

---

## ⚙️ Project Type Flags

- [x] Exploratory Data Analysis (EDA)
- [x] Dashboard / Data Visualization
- [x] Data Pipeline / ETL
- [x] Data Cleaning / Wrangling
- [x] End-to-End (multiple of the above)


---

## Table of Contents
1. [Project Overview](#1-project-overview)
2. [Objectives](#2-objectives)
3. [Project Scope & Tools](#3-project-scope--tools)
4. [Data Workflow](#4-data-workflow)
5. [Data Model & Schema](#5-data-model--schema)
6. [Analysis & Metrics](#6-analysis--metrics)
7. [Key Insights](#7-key-insights)
8. [Recommendations](#8-recommendations)
9. [Assumptions & Limitations](#9-assumptions--limitations)
10. [Portfolio Summary](#10-portfolio-summary)
11. [Author](#11-author)

---

## 1. Project Overview

**Context:** 
A survey was conducted among data professionals to better understand their career backgrounds, salaries, programming language preferences, demographics, job satisfaction, and experiences entering the data industry. The raw survey data contained a mixture of structured responses and free-text answers, making it useful for practicing real-world data preparation and visualization.

**Problem Statement:**
The raw survey data contained inconsistent and difficult-to-analyze responses, particularly around job titles, programming languages, salary ranges, industries, and countries. The goal was to transform the raw data into a cleaner dataset and create an interactive Power BI dashboard that could highlight meaningful patterns across data professionals.

**Approach:**
Approach:
The dataset was imported into Power BI and transformed using Power Query. Selected fields were cleaned and simplified, salary ranges were converted into approximate average salary values, and an interactive dashboard was created to explore salaries, job roles, programming languages, demographics, job satisfaction, and difficulty entering the data field.

**Outcome:**
The project produced an interactive Power BI dashboard containing key metrics, salary comparisons, programming-language preferences, country distribution, job satisfaction scores, gender-based salary comparisons, and perceptions of entering the data industry.

---

## 2. Objectives

- **Primary Objective:**
  Build an interactive Power BI dashboard that provides an overview of data professionals and their career characteristics.

- **Secondary Objective 1:**
  Clean and transform selected fields from the raw survey data so they could be effectively analyzed.
  
- **Secondary Objective 2:**
  Explore salary differences across job titles, countries, and gender.
  
- **Secondary Objective 3:**
  Understand respondents’ preferred programming languages and levels of job satisfaction.

---

## 3. Project Scope & Tools

### Scope

| Dimension | Details |
|-----------|---------|
| **In Scope** | Survey responses from data professionals, including job title, salary, programming language, country, gender, age, job satisfaction, and difficulty entering the data field |
| **Out of Scope** | Advanced normalization of every free-text response, predictive modeling, advanced statistical analysis, and extensive salary cleaning |
| **Time Period** | Survey collection period; exact dates were not specified in the transcript |
| **Granularity** | Individual survey respondent / row-level survey response |

### Tools & Technologies

| Category | Tool(s) Used |
|----------|-------------|
| Data Storage | CSV files |
| Data Processing | Power Query |
| Analysis | Microsoft Power BI |
| Visualization | Power BI |
| Version Control | GitHub |
| Other | Power BI calculated expressions |

---

## 4. Data Workflow

Overall Workflow
Raw Survey Data → Power BI → Power Query Cleaning → Data Transformation → Analysis → Interactive Dashboard

1. **Source:**
   The project used raw survey data collected from approximately 630 data professionals. The data was exported as a CSV file from the survey platform and made available through GitHub.
   
2. **Ingestion:**
   The CSV dataset was imported directly into Power BI and loaded into Power Query Editor for preparation before being used in the report.
   
3. **Cleaning:**
   
   Several data-quality issues were identified in the raw dataset, including:
- Inconsistent job-title responses
- Free-text “Other” responses
- Multiple variations of programming languagesranges stored as text
- Country and industry responses containing additional “Other” descriptions
- Salary values containing K, dashes, and plus signs
- Instead of extensively standardizing every response, the project simplified selected categories to make the dashboard manageable.

4. **Transformation:**
   
   Key transformations included:
- Splitting job-title responses using a delimiter
- Grouping detailed “Other” job titles into an Other category
- Splitting programming-language responses to isolate the main category
- Creating a duplicate salary field for transformation
- Splitting salary ranges into separate numeric components
- Removing K, dash, and plus characters from salary values
- Converting salary components into numeric values
- Creating an Average Salary field by averaging the lower and upper salary values
- Converting the resulting salary field into a numeric data type
- Simplifying country and industry responses

---

## 5. Data Model & Schema

 Data Professional Survey

The project used a single primary dataset, so there were no table joins or relationships involved.

### Dataset / Table

| Field Name | Data Type | Description | Example Value |
|------------|-----------|-------------|---------------|
| Unique ID | string | Unique identifier for each survey respondent | Respondent ID |
| Date Taken | date | Date the survey was completed | Survey date |
| Job Title | text | Respondent’s current professional role | Data Analyst |
| Current Yearly Salary | text | Original salary response, often represented as a range | 106-125k |
| Average Salary | numeric | Approximate salary calculated from the salary range | 115,500 |
| Industry | text | Industry where the respondent works | Technology |
| Favorite Programming Language | text | Programming language selected by the respondent | Python |
| Work-Life Balance | numeric | Respondent’s satisfaction score | 7 |
| Salary Happiness | numeric | Satisfaction with current salary | 5 |
| Coworker Happiness | numeric | Satisfaction with coworkers | 8 |
| Management Happiness | numeric | Satisfaction with management | 6 |
| Upward Mobility | numeric | Satisfaction with career advancement opportunities | 5 |
| Learning New Things | numeric | Satisfaction with learning opportunities | 8 |
| Difficulty Breaking Into Data | text | Respondent’s perception of entering the data field | Difficult |
| Gender | text | Respondent’s gender response | Female |
| Country | text | Country of the respondent | United States |
| Age | numeric | Respondent’s age | 29 |

> **Approximate row count:** 630 respondents


---

## 6. Analysis & Metrics

### Analytical Approach

The project followed an exploratory and descriptive analysis approach.
 Rather than attempting to predict future outcomes, the analysis focused on identifying patterns and differences within the survey responses.

The dashboard used segmentation and aggregation to compare respondents by job title, programming language, country, gender, salary, and job satisfaction.

### Key Metrics Defined

| Metric | Plain-Language Definition | Why It Matters |
|--------|--------------------------|----------------|
| Survey Takers | Total number of people who completed the survey | Provides the overall sample size |
| Average Age | Average age of survey respondents | Provides demographic context |
| Average Salary | Approximate average salary based on reported salary ranges | Allows salary comparisons across groups |
| Average Salary by Job Title | Average reported salary for each role | Highlights differences between data careers |
| Favorite Programming Language | Number of respondents selecting each programming language | Shows which technologies were most commonly preferred |
| Work-Life Balance Happiness | Average satisfaction score for work-life balance on a 0–10 scale | Measures perceived work-life balance] |
| Salary Happiness | Average satisfaction score relating to salary | Shows how satisfied respondents were with compensation |
| Average Salary by Gender | Average salary grouped by gender | Allows a basic comparison of reported compensation |
| Difficulty Breaking Into Data | Distribution of responses about entering the data field | Shows how accessible respondents perceived the industry to be |
| Country Distribution | Distribution of respondents by country | Provides geographic context for salary and career comparisons |


### Methods Used

- Descriptive statistics
- Average calculations
- Count and respondent aggregation
- Group comparison by job title
- Group comparison by gender
- Geographic segmentation
- Category distribution analysis
- Survey satisfaction analysis
- Interactive filtering through Power BI visualizations
  
---

## 7. Key Insights

**Insight 1:  Data Scientist Respondents Reported the Highest Average Salary**
Within the survey sample, Data Scientists had the highest reported average salary, followed by Data Engineers and Data Architects. Data Analysts represented a large share of respondents and had a lower average salary than these roles.

This suggests that role specialization and career path may be associated with significant differences in reported compensation.

**Insight 2: Python Was the Most Popular Programming Language**
Python was clearly the most frequently selected programming language in the survey, followed by languages such as R, JavaScript, Java, and C++.

This indicates that Python was particularly prominent among the professionals represented in this dataset.

**Insight 3: Country Had a Major Impact on Salary Comparisons**
The dashboard showed noticeable salary differences when respondents were filtered by country. For example, reported salaries for similar roles were substantially different between the United States and India.

This reinforces the importance of considering geographic context when comparing salaries.

**Insight 4 : Salary Satisfaction Was Relatively Low**
The salary satisfaction gauge showed that respondents were not particularly satisfied with their compensation compared with the 0–10 scale used in the survey.

This suggests that compensation may be an area where many respondents see room for improvement.

**Insight 5 : Breaking Into Data Was Not Perceived as Easy by Everyone**
Responses ranged from Very Difficult to Very Easy, with respondents spread across the different difficulty categories.

This highlights that entering the data profession can be perceived very differently depending on an individual’s background and circumstances.

**Insight 6 : Reported Average Salaries Were Similar Across Gender Groups**
The dashboard showed relatively similar average reported salaries between male and female respondents, with the female group slightly higher in this particular sample.

This should be interpreted carefully because the survey sample and methodology do not establish a broader gender-pay conclusion.

---

## 8. Recommendations


| Priority | Recommendation | Based On | Suggested Owner |
|----------|---------------|----------|-----------------|
| High | Standardize job titles and programming-language responses before performing deeper analysis | Inconsistent free-text responses | Data Analyst / Data Engineer |
| Medium | Collect salary information using a standardized numeric field rather than free-text salary ranges | Salary values required transformation and approximation | Data Analyst |
| Low | Expand the dashboard with additional demographic and career analysis | Large amount of unused survey information | Data Analyst |

---

## 9. Assumptions & Limitations

### Assumptions
- Salary ranges were treated as representative of the respondent’s compensation range.
- The midpoint of a salary range was used as an approximate salary value.
- Responses categorized as “Other” were grouped together rather than individually standardized.
- Satisfaction scores were treated as numeric values on a 0–10 scale.
- The survey responses were treated as representative only of the collected sample.

### Limitations
- Salary is approximate: The average salary field was created by taking the midpoint of reported salary ranges. This is an estimation rather than the respondent’s exact salary.
- Limited data cleaning: The project intentionally performed only basic cleaning. Many job titles, programming languages, industries, and countries could be standardized further.
- Free-text responses: “Other” responses contained multiple variations that were not fully normalized.
- Potential sample bias: The survey was distributed through social media and professional networks, so the respondents may not represent the entire global data-professional population.
- Self-reported data: Salary, satisfaction, age, and other responses were provided directly by participants and were not independently verified.


---

## 10. Portfolio Summary

This project demonstrates an end-to-end Power BI workflow, starting with raw survey data and progressing through data ingestion, Power Query transformation, exploratory analysis, KPI development, and interactive dashboard design. The project also demonstrates an important real-world analytics skill: recognizing that data visualization is only as good as the data preparation behind it, while clearly documenting the assumptions and limitations of the analysis.

---

## 11. Author

**Adewole Fakoya**

Data Analyst
- 🔗 LinkedIn (https://www.linkedin.com/in/adewole-fakoya-7484a5149)]



---

*Last updated: [Month YYYY]*
*If this template helped you, consider starring the repository.*
