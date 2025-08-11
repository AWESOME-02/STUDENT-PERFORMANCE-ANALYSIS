# INTRODUCTION
This project focuses on analyzing student academic performance using Excel, Power BI and Structured Query Language (SQL). It demonstrates how structured data analysis can reveal insights into student success rates, subject performance, group comparison and more.
## PROJECT OVERVIEW
Understanding students performance is key to making informed academic decisions. This project uses a fictional dataset of 50 students and aims to:
- Identify to performing students.
- Analyze average grades across subjects.
- Compare academic success across groups.
- Visualize promotion and repetition trends.
- Provide actionable insights to help improve student outcomes.
## TOOLS USED
- Excel: Data cleaning, preprocessing, pivot tables and dashboard visualization..
- Power BI: Transforming data and interactive dashboard with slicer, filters and visuals.
- SQL (SQL Server): Querying the data, aggregations and insights generation.
## DATA CLEANING AND PREPARATION
- Excel was used to fill up total scores, average grade and consideration column to prepare dataset for analysis.
- Power Query was used to transform dataset for better use in Power BI.
- Ensured numeric formats for analysis.
## SQL ANALYSIS
Using SQL Server I was able to answer all analytic questions.
### All SQL queries used
```
CREATE DATABASE MY_WORK_DB
SELECT * FROM [dbo].[STUDENT EDITED TABLE]

---ANSWERING QUESTIONS---
--1 TOP 5 BEST SUDENTS BASED ON AVERAGE SCORE
SELECT TOP 5 STUDENT_NAME, AVERAGE_SCORE
FROM [dbo].[STUDENT EDITED TABLE]
GROUP BY STUDENT_NAME, AVERAGE_SCORE
ORDER BY AVERAGE_SCORE DESC

--2 PERFORMANCE DISTRIBUTION
SELECT
AVG(MATHS_GRADE) AS AVERAGE_MATHS,
AVG(ENGLISH_GRADE) AS AVERAGE_ENGLISH,
AVG(BIOLOGY_GRADE) AS AVERAGE_BIOLOGY,
AVG(PHYSICS_GRADE) AS AVERAGE_PHYSICS,
AVG(CHEMISTRY_GRADE) AS AVERAGE_CHEMISTRY
FROM [dbo].[STUDENT EDITED TABLE]

--3 COUNT OF STUDENT BY STATUS
SELECT [STATUS], COUNT(STUDENT_NAME) AS NUMBER_OF_STUDENT
FROM[dbo].[STUDENT EDITED TABLE]
GROUP BY [STATUS]
ORDER BY NUMBER_OF_STUDENT DESC

--4 STATUS BY GROUP
SELECT [GROUP], [STATUS], COUNT([STATUS]) AS NUMBER_OF_STUDENT
FROM[dbo].[STUDENT EDITED TABLE]
GROUP BY [GROUP], [STATUS]
ORDER BY NUMBER_OF_STUDENT 

--5 NEW VS OLD STUDENT PERFORMANCE
SELECT NEW_OLD_STUDENT,
AVG(MATHS_GRADE) AS AVERAGE_MATHS,
AVG(ENGLISH_GRADE) AS AVERAGE_ENGLISH,
AVG(BIOLOGY_GRADE) AS AVERAGE_BIOLOGY,
AVG(PHYSICS_GRADE) AS AVERAGE_PHYSICS,
AVG(CHEMISTRY_GRADE) AS AVERAGE_CHEMISTRY
FROM [dbo].[STUDENT EDITED TABLE]
GROUP BY NEW_OLD_STUDENT

--6 CONSIDERATION STATUS
SELECT [CONSIDERATION], COUNT(STUDENT_NAME) AS NUMBER_OF_STUDENT
FROM[dbo].[STUDENT EDITED TABLE]
GROUP BY [CONSIDERATION]
ORDER BY NUMBER_OF_STUDENT DESC
```
 ## CHALLENGES
- Slow rendering due to system performance.
- Formatting DAX measures for % values.
## INSIGHTS 
- Only 23 students were initially promoted however the aggregate of students promoted and those promoted on trial was 92%.
- Group A had the highest repeat rate.
- English had the lowest subject average, suggesting a need for improvement.
## FILES

## WHAT I LEARNED
- How to structure and clean real-world educational data.
- Creating dynamic dashboards in Excel and Power BI.
- Writing DAX measures for clean visuals.
## NEXT STEPS
- Use a larger dataset (1000+ students) for deeper trend analysis.
- Using finance or health data for more experience in different sectors.
- Try building predictive models with Python.
## CONTACT
If you are interested in collaborating, mentoring or have feedback:
Abubakar Alimat
Data analyst, engineer and lifelong learner.

alimatabu02@gmail.com

09049059310

Lagos, Nigeria
