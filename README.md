<h1>Filter with AND, OR, and NOT  </h1>




<h2>Task 1. Retrieve after hours failed login attempts </h2>
The team is investigating failed login attempts that were made after business hours. I want to retrieve this information from the login activity. I’ll identify all unsuccessful attempts after 18:00. <br>

The login_time column in the <i>log_in_attempts</i> table contains information on when login attempts were made. Office hours end at '18:00'<br>
The <i>success</i> column in the <i>log_in_attempts</i> table contains values of <i>TRUE</i> or <i>FALSE</i> to indicate whether the login was successful.<br> MySQL stores Boolean values as <i>1</i> for <i>TRUE</i>, and <i>0</i> for <i>FALSE</i>. This means that <i>TRUE</i> is represented as <i>1</i>, and <i>FALSE</i> represented as <i>0</i> in the <i>success</i> column.


<h2>Task 2. Retrieve login attemps on specific dates</h2>
The team is investigating a suspicious event that occurred on <i>'2022-05-09'</i>.<br> I want to retrieve all login attempts that occurred on this day and the day before <i>('2022-05-08')</i>.

The login_date column in the <i>log_in_attempts</i> table contains information on the dates when login attempts were made.
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<h2>Task 3. Retrieve login attempts outside of Mexico</h2>
The team is investigating logins that did not originate in Mexico. Note that the country field includes entries with <i>'MEX'</i> and <i>'MEXICO'</i>. I will use the <i>NOT</i> and <i>LIKE</i> operators and the matching pattern <i>'MEX%'</i>.
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<h2>Task 4. Retrieve employees in Marketing</h2>
The team is updating employee machines, I need to obtain the information about employees in the 'Marketing' department who are located in all offices in the East building (such as <i>'East-170'</i> or <i>'East-320'</i>).<br>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<h2>Task 5. Retrieve employees in Finance or Sales</h2>
The team needs to perform a different update to the computers of all employees in the Finance or the Sales department.
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<h2>Task 6. Retrieve all employees not in IT</h2>
The team needs to make one more update. This update was already made to employee computers in the Information Technology department. The team needs information about employees who are not in that department.<br>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

