# Project 8 - Pentesting Live Targets

Time spent: 19 hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: Session Hijacking/Fixation
Walkthrough:<img src="https://github.com/Charding96/CyberSecur-w8/blob/master/w8Assignment_1.gif?raw=true" width="800"> 

Steps:
1. Open any website red or green
2. In blue website go to login homepage and input random password and sumbit(should give you unsuccessful login)
3. use the given tool "public/hacktools/change_session_id.php"  
3. Go to red/green webpage and login-in. 
4. After that use the tool again ( it should give you different id address)
5. Copy that address and paste back to the blue web app
6. The attacker is now able to access the victims session.

Vulnerability #2: SQL Injection
Walkthrough:<img src="https://github.com/Charding96/CyberSecur-w8/blob/master/w8Assignment_2.gif?raw=true" width="800">

Steps:
1. Go the salesperson info pages with the format "?id=XX" in the url
2. Replace the id with 'OR SLEEP(5)=0--'(it should get a id such as '%27OR%20SLEEP(5)=0--%27'
3. Then go to another salesperson info pages and replace the id.

## Green

Vulnerability #1: User Enumeration
Walkthrough:<img src="https://github.com/Charding96/CyberSecur-w8/blob/master/w8Assignment_3.gif?raw=true" width="800">

Steps:
1. Go to Login Homepage input nonexistent username and a random password, the site's error message states "Log in was unsuccessful."
2. Using the given username "jmonroe99" a valid username shows a bold error
3. Incorrect username shows a not-bolded error

Vulnerability #2: Cross-Site Scripting
Walkthrough:<img src="https://github.com/Charding96/CyberSecur-w8/blob/master/w8Assignment_4.gif?raw=true" width="800">

Steps:
1. On green web app go to feedback and input the information
2. In the comment section input '<script>alert('Mallory found the XSS!');</script>' from the assignment example.
3. Submit the feedback then login web app and will receive an message. 


## Red

Vulnerability #1:Insecure Direct Object Reference 
Walkthrough:<img src="https://github.com/Charding96/CyberSecur-w8/blob/master/w8Assignment_5.gif?raw=true" width="800">

Steps:
1. The salesperson database can be accessed by change the "id=" tag in the url, 
2. Next access salespersons of id 10 and 11, while the publicly displayed data ends at id=9.

Vulnerability #2: Cross-Site Request Forgery
Walkthrough:<img src="https://github.com/Charding96/CyberSecur-w8/blob/master/w8Assignment_6.gif?raw=true" width="800">

Steps:
1. Log into the staff area to decide which form URL and data you want to forge.
2. Create a html file 
3. Save and open in browser 
4. Click Updateq


## Notes

The Cross-Site Request Forgery is diffcult.
