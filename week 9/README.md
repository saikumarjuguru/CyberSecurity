# Week 9 - Pentesting Live Targets

Time spent: 9 hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green and red.

## User Stories
The folowing six exploits need to be demonstrated:  

1. Username Enumeration 
2. Insecure Direct Object Reference (IDOR)  
3. SQL Injection (SQLi)  
4. Cross-Site Scripting (XSS)  
5. Cross-Site Request Forgery (CSRF)  
6. Session Hijacking/Fixation 

## Blue

1. Vulnerability #1: **SQL Injection (SQLi)**
	- Description:  
	The Attacker can inject a remote code execution command, in the value of 'id' in the URL, to cause a Denial of Service on the SQL database. In this case a sleep(5) command is being executed on the database.
	- GIF Walkthrough:  
	![](https://media.giphy.com/media/fSqkRaxT8aEO2gvHQg/giphy.gif)

2. Vulnerability #2: **Session Hijacking/Fixation**
	- Description:  
	The Attacker can obtain the victim's session ID and gain login access to the victim's account.
	- GIF Walkthrough:  
	![](https://media.giphy.com/media/kyFwe5JQl1xyI0q5UG/giphy.gif)

## Green

1. Vulnerability #1: **Username Enumeration**  
	- Description:  
		The developer uses different classes for when the error exists due to non-existent username (class="failed"), which is not defined in the /green/public/styles.css, but for other errors, the developer uses class="failure" which is described in the given styles.css.
	- GIF Walkthrough:  
	![](https://media.giphy.com/media/MdizewCzbbEr2BdAJd/giphy.gif)

2. Vulnerability #2: **Cross-Site Scripting (XSS)**
	- Description:  
		Attacker can inject an XSS in his/her feedback form.
	- GIF Walkthrough:  
	![](https://media.giphy.com/media/SSch10EkJxkXM8RFRq/giphy.gif) 

## Red

1. Vulnerability #1: **Insecure Direct Object Reference**
	- Description:  
		Attacker can get access to hidden users' accounts that the attacker is not permitted to view. It can be achieved through modifying 'id' parameter of the URL to change the GET request.
	- GIF Walkthrough:  
	![](https://media.giphy.com/media/ifB3MsYJwmK0lae75L/giphy.gif)
2. Vulnerability #2: **Cross Site Request Forgery** 
	- Description:  
		The attacker can create a malicious page that utilizes the user's session to forge a request to the database, and this page secretly makes a post request on page load and hides the outcome in a hidden iframe. As result, an account in the database is altered.    
	- GIF Walkthrough:  
	![](https://media.giphy.com/media/YqWjWpZogzwsnOp6lC/giphy.gif)

### Resources
GIFs created with [LiceCap](http://www.cockos.com/licecap/)

### License

	Copyright [2019] [Sai Kumar Juguru]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

