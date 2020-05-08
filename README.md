# Week 09 - Pentesting Live Targets

Time spent: **X** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:

* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each color is vulnerable to only 2 of the 6 possible exploits. First discover which color has the specific vulnerability, then write a short description of how to exploit it, and finally demonstrate it using screenshots compiled into a GIF.

## Blue

Vulnerability #1: Session Hijack

Description:

This attack took advantage of the PHP script that was left, and deployed a session hijack. A browser in google chrome was used to log in to a session. The PHP script was then loaded to gain access to the session ID. Then burp intercepted the login page of the site on a Firefox browser. There the session ID was changed to that of the logged in ID from the google browser and forwarded back to Firefox. The result was a successful log in using the hijacked session ID.

![](blue_session.gif)

Vulnerability #2: SQLI

Description: When editing the URL id number for the salesperson changin the number shows the respective representative. This is done fairly instantaneously. However, when the following SQL line is placed in the value for the id, the server takes several seconds to load, indicating it registers the command and can be infiltrated with other injections. 

>%27%20OR%20SLEEP(5)=0--%27

![](blue_sqli.gif)

## Green

Vulnerability #1: __________________

Description:

<img src="green-vuln1.gif">

Vulnerability #2: __________________

Description:

<img src="green-vuln2.gif">


## Red

Vulnerability #1: IDOR

Description:

After clicking on a representative in the Find a Salesperson menu, the URL will end in an id repsective to a representative. If the id is changed to 11 it will show data that would seem inappropriate for the public to access. The other color sites are protected from this vulnerability.

![](red_IDOR.gif)

Vulnerability #2: __________________

Description:

<img src="red-vuln2.gif">


## Notes

Describe any challenges encountered while doing the work
