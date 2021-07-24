# Pewlett_Hackard_Analysis

## Overview
The purpose of this analysis is to analyze the data provided from Pewlett Hackard to determine employee relationships based on employees retiring from the company. Pewlett Hackard is a large company and is looking toward the future as employees are retiring at a rapid rate. They are looking into the future by offering retirement packages for those that meet certain critera and thinking about which postions might need to be filled in the near future.
We used SQL to create a database and write several queries to sort, clean, and anlyze our data to provide accurate results.
The challenge consists of the following deliverables:
- Determine the number of retiring employees by job title
- Determine the employees eligible for the mentorship program
### Resources
- data: csv files located in the data folder
- Software: SQL / pgadmin
## Results
### Deliverable 1: Number of retiring employees by job title

- Frst, we joined the data from the employees and titles csv files and filtered by the employees birthdates from 1952 to 1955 to determine the retiring employees by title:

![image](https://user-images.githubusercontent.com/84201614/126881953-88994853-24b9-4f86-93c5-94d4f6d106ca.png)

- Then, we used a DISTINCT ON statement to eliminate duplicate employees that have switched titles over the years. We saved the data as unique_titles:

![image](https://user-images.githubusercontent.com/84201614/126882029-9be4fbe2-73c1-425a-b818-32693c198387.png)


- Lastly, we wrote another query to group the number of employees by their most recent job title who are about to retire. This data is saved as retiring_titles:

![image](https://user-images.githubusercontent.com/84201614/126882101-64ff1516-c809-465c-aa50-b85ea57360c4.png)

### Deliverable 2: Employees eligible for the mentorship program

- We created a mentorship_eligibility table by joining the employees and dept_emp data into the table and filtering on current employees and on employees born in 1965:

![image](https://user-images.githubusercontent.com/84201614/126882187-3dece2b1-27a6-46cc-8716-9064711970d0.png)

## Summary

Based on our results, we can see that senior engineers and senior staff have the highest count of retiring employees. This makes sense since these titles are most often occupied by individuals with more experience, hence older age. Managers are the least likely to retire, therefore, retirement packages and replacemement concerns are not as frequent. Based on our mentorship eligibility data, we can see that senior staff and engineers are the most likely to be eligible for the program. Assistant engineers are the least likely to qualify. This data also makes sense that the company would want to invest their resources in younger employees (engineers) that will stay at the company long enough to yield results. It may be useful to filter the data on different birth dates to analyze other employees leaving the company other than those soley leaving for retirement reasons.      

In addition to the mentorship eligiblity table, here is a table for the same data grouped by title:
![image](https://user-images.githubusercontent.com/84201614/126882524-470c470c-abdc-4bd5-8fc2-b94d62956b56.png)
