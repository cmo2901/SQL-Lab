# Querying Databases with SQL and SQL Filters


## Objective
In this lab, I serve as an analyst for an organization looking to maintain their security posture. Using SQL queries with filters, I will accomplish two tasks: gather information on anomalous login attempts based on timeframe and location, and take inventory on what machines may need security updates. 

### Tools Used
Database lab environment provided by Google

### Skills Learned
<p> SQL<br>
SQL Queries<br>
SQL Filters</p>


### Retrieving login attempts from after-hours
<p> To investigate a potential security incident, I needed to query the logins database for login attempts made after regular business hours. To filter my query, I used 'success = FALSE' and 'login_time > '18:00.' By placing the AND operator between these two conditions, I only retrieved results that meet both conditions:</p>

<img width="677" alt="After hours failed login attempts" src="https://github.com/user-attachments/assets/2fd749b6-f23c-40bd-acf4-a7121ed97e17" />


### Retrieving login attempts from specific dates
<p> I needed to investigate an event that happened on 2022-05-09. I queried the login database for all login attempts from 2022-05-09 and 2022-05-08. To do so, I set 'login_date' equal to each of these dates, then placed the OR operator between the two conditions: </p>

<img width="761" alt="Login attempts by specific date" src="https://github.com/user-attachments/assets/15fa2c90-be5e-4ab4-b21d-a3352c4aa031" />


### Retrieving login attempts based on geographic location
<p> The security event likely did not occur in Mexico, so I needed to query the database for login attempts made outside of Mexico. The database sometimes stores 'Mexico' as 'MEX,' so I used the NOT and LIKE operators along with the % wildcard in my filter:</p>

<img width="578" alt="Login attempts outside of Mexico" src="https://github.com/user-attachments/assets/9b2b8426-f38a-4526-a376-3c7c257bbef3" />

### Taking inventory of machines by department and building
<p> To get inventory of all machines in the marketing department from a specific building, I utilized the AND operator to filter by department and office. Using the LIKE operator and % wildcard, I retrieved results for all offices in the east building:</p>

<img width="708" alt="Marketing machines East office" src="https://github.com/user-attachments/assets/59526bb6-4bc4-491c-9dc4-456131a7af90" />


### Taking inventory of machines in Finance or Sales departments
<p>To gather machine information in the Finance and Sales departments, I filtered my query using the OR operator to return results that meet either condition:</p>

<img width="667" alt="Finance and sales machines" src="https://github.com/user-attachments/assets/f89e9902-b620-41e5-a7be-19009fa17b2f" />

### Retrieve all non-IT department machines
<p>I was able to retrieve results for all non-IT machines by using the NOT operator:</p>

<img width="642" alt="Non IT machines" src="https://github.com/user-attachments/assets/69c18382-704c-4d92-a80e-d9d1c8771c48" />


