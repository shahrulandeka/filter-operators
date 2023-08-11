<h1>[Mini] Filter with AND, OR and NOT operators</h1>

<h2>Description</h2>
In this lab example, I run through how to filter with AND, OR and NOT operators. I 'll have to find specific data that depends on one or more factors. I can use these operators to create more complex filters in SQL queries. <br/>
For this example, I need to obtain specific information about employees, their machines and the department they belong to from the database. My team needs data to investigate potential security issues and to update computers. <br/>
 <br/>
At the end of this lab, I have practical experience in using SQL to: <br/>
- Run SQL queries to retrieve information from a database and, <br/>
- Apply AND, OR and NOT operators to filter SQL queries.

<h2>Languages and Utilities Used</h2>

- <b>Bash Shell</b> 
- <b>Oracle VM Virtual Box</b>

<h2>Environments Used </h2>

- <b>Windows 10 Pro</b> (22H2)

<h2>Program walk-through:</h2>

<p align="center">
Launch the utility: <br/>
For this example, I am responsible for filtering the required information from the database. <br/>
Firstly, I'll have to retrieve failed login attempts after business hours. <br/>
Second, I'll retrieve login attempts that occured on specific dates. <br/>
Third, I'll retrieve logins that didn't originate from Mexico. <br/>
Fourth, I'll retrieve information about certain employees in the Marketing department. <br/>
Fifth, I'll retrieve information about employees in the Finance or the Sales department. <br/>
Finally, I'll obtain information about employees who are not in the Information Technology department. <br/>
<img src="https://i.imgur.com/mW86utj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
1. For this task, I am retrieving the failed login attempts after business hours.: <br/>
To query the database, type in: <br/>
 SELECT * <br/>
 FROM log_in_attempts <br/>
 WHERE login_time > '18:00' AND success = false; <br/>
 Note* The "*" symbol signifies selecting ALL from the table. Whereas we put the success as "false" to signify failed login attempts. <br/>
<img src="https://i.imgur.com/uQKSDZE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
2. For this task, I am investigating a suspicious event that occured on '2022-05-09': <br/>
 I want to retrieve all login attempts that occured on this day and the day before ('2022-05-08'). <br/>
 To retrieve this set of require info, type in: <br/>
 SELECT * <BR/>
 FROM log_in_attempts <br/>
 WHERE login_date = '2022-05-09' OR login_date = '2022-05-08';
<img src="https://i.imgur.com/UBaR6iC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
3. To find countries other than Mexico, type in: <br/>
 SELECT * <BR/>
 FROM log_in_attempts <br/>
 WHERE NOT country LIKE 'ME%'; <br/>
 Note* The '%' sign is used as a wildcard.
<img src="https://i.imgur.com/uIAbuBl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
4. I'm writing an SQL query to retrieve records for employees in the 'Finance' or the 'Sales' department: <br/>
 SELECT * <BR/>
 FROM employees <br/>
 WHERE department = 'finance' OR department = 'sales';
<img src="https://i.imgur.com/83ea1ME.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
5. To retrieve all employees who are NOT in IT:  <br/>
 SELECT * <br/>
 FROM employees <br/>
 WHERE NOT department = 'Information Technology';
<img src="https://i.imgur.com/W3aDJDe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
