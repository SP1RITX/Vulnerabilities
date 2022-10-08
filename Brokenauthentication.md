# Broken authentication 

## What is Broken Authentication ?

Broken authentication is a term describing multiple vulnerabilities threat actors exploit to impersonate legitimate users online. It refers to weaknesses in session and credential management. Attackers can use both to mimic an authorized user using hijacked session IDs or stolen login credentials

![image](https://user-images.githubusercontent.com/72333625/194703655-3aa37fff-031f-4ab5-9097-8ce944130752.png)

## BUG:

Session Never expires after log out from website

### Steps:

1. Login into the website

2. Then visit some website pages and then logout from website

3.  After that you can see login  page then press back button

4. You can see your account still open

5. you can see only previous pages and interact with it

### Solution:

Session ID should expire immediately after logout

## Additional 

Once you logout 

