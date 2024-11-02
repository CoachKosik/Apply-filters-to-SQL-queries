# Apply filters to SQL queries

## Objective

To leverage SQL queries and advanced filtering techniques to enhance system security and incident response. By effectively analyzing and filtering data, I can identify potential security threats, investigate anomalies, and implement necessary security measures. This project demonstrates my ability to use SQL to extract valuable insights from large datasets, enabling proactive security measures and efficient incident response.

## Project description
As part of my role in fortifying our organization's system security, I am tasked with ensuring the integrity of the system, conducting thorough investigations of potential security vulnerabilities, and performing necessary updates on employee computers. The following examples illustrate how I have employed SQL with advanced filtering techniques to address and manage security-related tasks effectively.

## Skills Learned

Technical Skills:
* SQL Querying:
  * proficiency in constructing complex SQL queries to filter and retrieve specific data.
  * used operators like AND, OR, NOT, and LIKE to refine search criteria.
  * demonstrated an understanding of database structures and relationships to effectively join tables.
* Data Analysis:
  * analyzed the results of SQL queries to identify trends, anomalies, and potential security risks.
  * used data analysis to inform decision-making and prioritize security efforts.
* Security Awareness:
  * demonstrated an understanding of common security threats, such as unauthorized login attempts.
  * applied knowledge to identify and mitigate potential security risks.

*Soft Skills:
  * Problem-Solving: identified a security problem and devised a solution using SQL queries.
  * Critical Thinking: analyzed the data and drawn logical conclusions to address the security issue.
  * Attention to Detail: carefully crafted SQL queries to ensure accurate and reliable results.
  * Effective Communication: clearly explained your approach and findings, both in written and visual formats.

Effectively utilizing SQL queries, demonstrats a strong foundation in database management and data analysis. Showcasing invaluable skills in various cybersecurity roles, including incident response, threat intelligence, and security operations.

## Tools Used

1. SQL Database Management System (DBMS):

* The DBMS provides the database engine to store and manage the data.

2. SQL Client:

* A tool to interact with the database and execute SQL queries. This could be a command-line tool like mysql or a graphical user interface (GUI) tool like SQL Developer or DBeaver.

3. Text Editor:

A text editor (e.g., Notepad++, Sublime Text, Visual Studio Code) is used to write and edit SQL queries.
Key SQL Concepts Used:

SELECT: Used to retrieve specific data from the database.
WHERE: Used to filter data based on specific conditions.
AND, OR, NOT: Logical operators used to combine multiple conditions.
LIKE: Used for pattern matching in string comparisons.
Date and Time Functions: Used to filter data based on specific time periods.

## Steps
### **Retrieve after-hours failed login attempts**

In the event of a potential security incident occurring after business hours (post-18:00), it is essential to investigate all failed login attempts during this period. The following SQL query exemplifies how I utilized advanced filtering techniques to identify and analyze failed login attempts that transpired outside of regular business hours.

The following SQL query was utilized to identify and analyze failed login attempts that occurred outside of standard business hours, enabling us to proactively address potential security breaches:<br>

![sql 1](https://github.com/user-attachments/assets/ff56dae3-3c3a-4064-b487-b5cda3106bce)<br>

The provided SQL query effectively filters for failed login attempts that occurred after 6 PM. By utilizing the WHERE clause with the AND operator, I was able to isolate relevant data from the log_in_attempts table. The first condition, login_time > '18:00', ensures that only login attempts after 6 PM are considered. The second condition, success = FALSE, further refines the results to include only unsuccessful login attempts.

### Retrieve login attempts on specific dates

To identify potential security breaches, I conducted a thorough investigation of login activity surrounding May 9, 2022. This involved querying our database for any login attempts that occurred on or before this date.

The following SQL query demonstrates how I effectively filtered for login attempts that occurred within a specific timeframe, enabling a more targeted analysis of potential security breaches:<br>

![sql 2](https://github.com/user-attachments/assets/d8a7688d-ae16-4651-aad0-f936b7b93724)<br>

### Retrieve login attempts outside of Mexico

Following an in-depth analysis of login attempts, I identified an anomaly in login activity originating from locations outside of Mexico. To mitigate potential security risks, I recommend further investigation into these anomalous login attempts.

The following SQL query demonstrates how I effectively filtered for login attempts originating from locations outside of Mexico:<br>

![sql 3](https://github.com/user-attachments/assets/386e502d-ede1-44fc-a454-db1588dd6e8d)<br>

The first portion of the screenshot displays my SQL query, while the second part shows a portion of the resulting output. This query effectively identifies all login attempts originating from countries outside of Mexico. 

To achieve this, I began by selecting all data from the log_in_attempts table. Subsequently, I employed a WHERE clause with a NOT operator to filter out records associated with Mexico. The LIKE operator, paired with the wildcard character (%), was utilized to match both 'MEX' and 'MEXICO' within the country field.

### Retrieve employees in Marketing

To streamline the process of updating employee computers within the Marketing department, I utilized SQL queries to identify specific machines in need of upgrades. This data-driven approach ensured efficient and targeted deployment of updates.

The following SQL query demonstrates how I effectively filtered for employee machines belonging to the Marketing department, specifically those located in the East building:<br>

![sql 4](https://github.com/user-attachments/assets/c66bbcbf-3628-4658-9595-976666c886ec)<br>

The SQL query below effectively isolates employees within the Marketing department located in the East building. By employing a WHERE clause with AND operators, we can specify multiple conditions to refine the search. In this instance, we've utilized the LIKE operator with the 'East%' pattern to match the 'office' column, ensuring accurate identification of employees in the desired location.

SELECT *
FROM employees
WHERE department = 'Marketing' AND office LIKE 'East%';

### Retrieve employees in Finance or Sales
To ensure the security of our Finance and Sales departments, I utilized SQL queries to identify the specific employees requiring the necessary security updates. By filtering the data based on department criteria, I effectively targeted the required systems for timely patching.

The following SQL query demonstrates how I effectively filtered for employee machines belonging to individuals within the Finance and Sales departments: <br>

<b![sql 5](https://github.com/user-attachments/assets/7ae951dc-6f6a-4c55-a87a-4a1062c027c9)r>

The provided SQL query effectively retrieves employees from both the Finance and Sales departments. By employing the `WHERE` clause with the `OR` operator, the query efficiently identifies individuals who belong to either department. This demonstrates a strong understanding of SQL's filtering capabilities and its application in real-world security scenarios.

### Retrieve all employees not in IT

To identify employees outside the Information Technology department who require critical security updates, I utilized SQL queries to filter and extract relevant data. This targeted approach ensures that necessary security measures are implemented efficiently and effectively.

Here's an example of how I utilized SQL to identify potential vulnerabilities within our system. By filtering employee machines that do not belong to the IT department, I was able to prioritize security efforts and allocate resources effectively:<br>

![sql 6](https://github.com/user-attachments/assets/8aa5eb59-c811-4ff6-afb9-64b2a48b1a2a)<br>

### Summary

To enhance our organization's security posture, I employed SQL queries with advanced filtering techniques to analyze login attempts and employee machine data. By joining the 'log_in_attempts' and 'employees' tables and utilizing operators like AND, OR, NOT, and the wildcard character (%), I was able to extract critical insights, identify anomalies, and take appropriate actions. 

## Materials Provided
<a href="https://docs.google.com/document/d/12wldwY7MB49m1PgouLjjarlcc1Ty1pf3FqNOfK4RBQE/edit?usp=sharing">File permissions in Linux</a><br>
<a href="https://docs.google.com/document/d/1sBEeC5_8Uf_sHgOabpFd497VMQIm_Q3h/edit?usp=sharing&ouid=105064495821226407439&rtpof=true&sd=true">Current file permissions of the /home/researcher2/projects directory</a>
