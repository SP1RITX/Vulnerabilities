# What is Access control vulnerability ?
Access control (or authorization) is the application of constraints on who (or what) can perform attempted actions or access resources that they have requested. In the context of web applications, access control is dependent on authentication and session management:

Authentication identifies the user and confirms that they are who they say they are.
Session management identifies which subsequent HTTP requests are being made by that same user.
Access control determines whether the user is allowed to carry out the action that they are attempting to perform

Access control design decisions have to be made by humans, not technology, and the potential for errors is high.

From a user perspective, access controls can be divided into the following categories:

* Vertical access controls
* Horizontal access controls
* Context-dependent access controls

# Steps used to perform access control on the target website .
1. First we Found out where to perform access control 
2. The Target we get are (/admin , /User/ChangePassword/43600880-d842-4f82-bba3-4502de19f0d5 )
3. We will use burpsuite to make request on that page
4. When we Go to that page we will get know that I does't allow any access
5. We can't find anything 

# POSTED
GET /User/ChangePassword/43600880-d842-4f82-bba3-4502de19f0d5 HTTP/1.1

Host: magnus.jalatechnologies.com

User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:78.0) Gecko/20100101 Firefox/78.0

Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8

Accept-Language: en-US,en;q=0.5

Accept-Encoding: gzip, deflate

Connection: close

Referer: https://magnus.jalatechnologies.com/Home/Index

Cookie: _ga=GA1.2.1847537744.1665136688; _ga_97T86CNKZ0=GS1.1.1669488192.15.1.1669488908.0.0.0; __RequestVerificationToken=oKVA50oKj614kz6krJ9ZQCS8bmalegEC_bnQ7Mx1Pc4gaaxF0sytagA2gQ4kshgH0M4GpmqPS-sPgY9tcWSK0-eH72vW8ZFzyQiX66ePPlM1; ASP.NET_SessionId=k4afvlkds2i5q3onr3x4p0wm; _gid=GA1.2.179272554.1669488192; .ASPXAUTH=21333B22AD33826BE781D6B0077B54181540F445F9446D78609868A10755B81A125D8AC4C8F7D82FD1947BA0163822E68F997CEC58D7F8D633D61E58EFB77C457B4EAE5A0D1E94C17F6ECA43608E31838E0E31A3647991C158843615391FC1069969B05EDCF5F191A7F50E208CD70B5A458D35C86B835AD667E7BD9D6F0EA3DD; _gat_gtag_UA_131080393_1=1

Upgrade-Insecure-Requests: 1


## RESPONSE
HTTP/1.1 302 Found

Cache-Control: private

Content-Type: text/html; charset=utf-8

Location: /Account/Login

Server: Microsoft-IIS/8.5

X-AspNetMvc-Version: 5.2

X-AspNet-Version: 4.0.30319

X-Powered-By: ASP.NET

X-Powered-By-Plesk: PleskWin

Date: Sat, 26 Nov 2022 19:06:53 GMT

Connection: close

Content-Length: 131



<html><head><title>Object moved</title></head><body>

<h2>Object moved to <a href="/Account/Login">here</a>.</h2>

</body></html>


## How to prevent access control vulnerabilities ?
Access control vulnerabilities can generally be prevented by taking a defense-in-depth approach and applying the following principles:

Never rely on obfuscation alone for access control.
Unless a resource is intended to be publicly accessible, deny access by default.
Wherever possible, use a single application-wide mechanism for enforcing access controls.
At the code level, make it mandatory for developers to declare the access that is allowed for each resource, and deny access by default.
Thoroughly audit and test access controls to ensure they are working as designed.




