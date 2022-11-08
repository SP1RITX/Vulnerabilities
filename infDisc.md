# Information disclosure

# What is Information Disclosure Vulnerabilty ?
Information disclosure, also known as information leakage, is when a website unintentionally reveals sensitive information to its users. Depending on the context, websites may leak all kinds of information to a potential attacker, including:

* Data about other users, such as usernames or financial information
* Sensitive commercial or business data
* Technical details about the website and its infrastructure
 
 ![image](https://user-images.githubusercontent.com/72333625/200650049-3c713227-f67c-4665-b155-a391bc204adc.png)

# Steps to peform 
1. Do a Dirb scan on the website(For me I am using Dirsearch)
2. Command used ( Dirsearch -u https://magnus.jalatechnologies.com/ ) 
3. Open Directory Found on the wesbite are 
 * /favicon.ico (Nothing interseting)
 * /account (redirect to login page)
 * /account/ (Redirect to login page)
 * /account/login (Redirect to login page)
 * /\..\..\..\..\..\..\..\..\..\etc\passwd(403)
 * /Trace.axd (Somewhat usefull)

## What is Trace.axd ?
The Trace. axd application keeps a very detailed log of all requests made to an application over a period of time. This information includes remote client IP's, session IDs, all request and response cookies, physical paths, source code information, and potentially even usernames and passwords.

## Trace.axd IMPACT
ASP.NET's trace feature is a powerful mechanism that helps developers debug and resolve problems in their applications, but it can also be used by attackers to gain information about requests and responses to the application. An attacker can obtain information such as:
* Session cookies
* Session state
* Query string and POST variables
* Physical path of the requested file
* Execution time
This means that the attacker can hijack almost every active user's session by using their session details.

![image](https://user-images.githubusercontent.com/72333625/200652838-4fd033a8-80e5-4862-88fd-5c4584012c37.png)
