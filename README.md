# Pewlett-Hackard-Analysis

## Analysis Overview

The goal of this analysis required us to first complete the following tasks: 
* Determine the number of retiring employees per title 
* Identify employees who are eligible to participate in a mentorship program

Following completion of the tasks noted above, we summarized our analysis to help prepare for the “silver tsunami” as many current employees reach retirement age.

### Resources
* Data Files: 
  * departments.csv
  * dept_emp.csv
  * dept_manager.csv
  * employees.csv
  * salaries.csv
  * titles.csv

* Data Analysis Tools:
  * SQL
  * PostgreSQL
  * pgAdmin

## Analysis Results

### The Number of Retiring Employees by Title

* First step was to create the unique_titles table by joining the employees and titles tables together to compile the data for this analysis. 
* Second step was to narrow the scope of our analysis, we filter by date of birth and date hired then removed the duplicates from the joined table, and sorted the data points by date hired. 
* A total of 90,398 employees are retiring per the above criterion we set for our analysis.
* The number of employees leaving by title: 
  * 29,414 Senior Engineers
  * 28,254 Senior Staff
  * 14,222 Engineers
  * 12,243 Staff
  * 4,502 Technique Leaders
  * 1,761 Assistant Engineers
  * 2 Managers

![image](https://user-images.githubusercontent.com/96931376/161870939-9f29a138-eebe-4cf5-a419-ec45597a99a0.png)

### The Employees Eligible for the Mentorship Program

* First step was to create the mentorship_eligibility table by joining the following tables: employees, department employees, and titles tables.
* Second step was to narrow the scope of our analysis to employees that actually qualify for the retiring/mentorship package, we focused on employees that were born in 1965.
* A total of 1,549 employees are eligible per the above criterian we set for our analysis.
* The number of eligible employees by title: 
  * 402 Engineers
  * 392 Senior Staff
  * 332 Staff
  * 290 Senior Engineers
  * 77 Technique Leaders
  * 56 Assistant Engineers

![image](https://user-images.githubusercontent.com/96931376/161870974-99b2ab8e-9fda-47b2-958c-32066120d86b.png)

## Analysis Summary

To better prepare for the "silver tsunami," our recommendation is to narrow the scope to the 13,505 employees that currently work at the company, have been there since 1985 to 1988, and their birth date is between 1962 and 1965. This is the selection of employees that would be considered eligible for the mentorship program to educate new hires as they transition into retirement. This data analysis can be used to chart timelines for employee departures, replacement hires, and training period.

To be better prepared to hire replacements for the departing employees: 

![image](https://user-images.githubusercontent.com/96931376/161872012-de724737-1ed0-48fa-b820-266cba9cd8c2.png)

Another recommendation would be to verify that there are the required number of potential mentors across all departments. To determine this recommendation, the employees_leaving table is recreated with the department each employee belongs to added on.

![image](https://user-images.githubusercontent.com/96931376/161872049-a1169899-76db-491c-932d-62913ab6af32.png)

Next, we organize the table of employees that are leaving by their departments to determine the collect that total. 

![image](https://user-images.githubusercontent.com/96931376/161872081-904a5cd5-d771-4478-a318-8569c73e3cc6.png)

A variable to further investigate the incorporation of this mentorship program into the company is the willingness or ability of retiring employees to participate. This variable could be mitigated as a potential risk if it's properly timed with the projected retirement date and future hire date. Based on the pattern of results, approximately 25% of retiring employees are expected to have the opportunity to participate in the mentorship program to facilitate an efficient transition to the new hire.
