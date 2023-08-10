<h1>[Mini] Filter with AND, OR and NOT operators</h1>

<h2>Description</h2>
In this lab example, I run through how to filter with AND, OR and NOT operators. It's likely that I 'll have to find specific data that depends on one or more factors. I can use these operators to create more complex filters in SQL queries. <br/>
For this example, I need to obtain specific information about employees, their machines and the department they belong to from the database. My team needs data to investigate potential security issues and to update computers. <br/>
 <br/>

<h2>Languages and Utilities Used</h2>

- <b>Bash Shell</b> 
- <b>Oracle VM Virtual Box</b>

<h2>Environments Used </h2>

- <b>Windows 10 Pro</b> (22H2)

<h2>Program walk-through:</h2>

<p align="center">
Launch the utility: <br/>
<img src="https://i.imgur.com/n9gSzhj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
1. Firstly, we would use the pwd command to know which directory we are currently working in:
 <br/>
  For this example, we would use cd command to switch into the "logs" directory.
  <br/>
  Then, use the ls command to list the content of the current directory.
  <br/>
  Use the grep command to filter the server_logs.txt file, and return all lines containing the text string "error".
<img src="https://i.imgur.com/SdOSXv9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
2. Now we want to navigate to the /home/analyst/reports/users directory: <br/>
  Type in cd . . to go up one directory. <br/>
  Type in cd reports, followed by cd users to reach the correct directory. <br/>
  Using the pipe character ( | ), pipe the output of the ls command to the grep command to list only the files <br/> containing the string Q1 in their names.
<img src="https://i.imgur.com/gr6Unl2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
3. Let's try this again:  <br/>
  List the files that contain the word access in their names
<img src="https://i.imgur.com/ZuadzTc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
4. For this example, let's search for information contained in user files and report on users<br/>
  that were added and deleted from the system:  <br/>
  Use ls command to list the files in the current working directory. <br/>
  Suppose we are looking for someone called jhill. Search the Q2_deleted_users.txt file for the username jhill.
<img src="https://i.imgur.com/Gln5x9W.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
5. Suppose we want to find out how many users were added to the Human Resource department in Q4:  <br/>
For shortcut, i used the cat command to list the content of Q4_added_users.txt <br/>
  From there we can see there are 2 users added to the HR department in Q4.
<img src="https://i.imgur.com/DcfFbOb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
