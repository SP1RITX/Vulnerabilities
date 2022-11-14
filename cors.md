# What is CORS (Cross-origin Resource sharing) ?
Cross-origin resource sharing (CORS) is a browser mechanism which enables controlled access to resources located outside of a given domain. It extends and adds flexibility to the same-origin policy (SOP). However, it also provides potential for cross-domain attacks, if a website's CORS policy is poorly configured and implemented. CORS is not a protection against cross-origin attacks such as cross-site request forgery (CSRF).
![image](https://user-images.githubusercontent.com/72333625/201738168-63616d52-702b-4953-b3b2-d5c927d579b1.png)

# Vulnerabilities arising from CORS configuration issues
Many modern websites use CORS to allow access from subdomains and trusted third parties. Their implementation of CORS may contain mistakes or be overly lenient to ensure that everything works, and this can result in exploitable vulnerabilities.

# How to prevent CORS-based attacks
CORS vulnerabilities arise primarily as misconfigurations. Prevention is therefore a configuration problem. The following sections describe some effective defenses against CORS attacks.

# Proper configuration of cross-origin requests
If a web resource contains sensitive information, the origin should be properly specified in the Access-Control-Allow-Origin header.

# Only allow trusted sites
It may seem obvious but origins specified in the Access-Control-Allow-Origin header should only be sites that are trusted. In particular, dynamically reflecting origins from cross-origin requests without validation is readily exploitable and should be avoided.

# Avoid whitelisting null
Avoid using the header Access-Control-Allow-Origin: null. Cross-origin resource calls from internal documents and sandboxed requests can specify the null origin. CORS headers should be properly defined in respect of trusted origins for private and public servers.

# Avoid wildcards in internal networks
Avoid using wildcards in internal networks. Trusting network configuration alone to protect internal resources is not sufficient when internal browsers can access untrusted external domains.

# CORS is not a substitute for server-side security policies
CORS defines browser behaviors and is never a replacement for server-side protection of sensitive data - an attacker can directly forge a request from any trusted origin. Therefore, web servers should continue to apply protections over sensitive data, such as authentication and session management, in addition to properly configured CORS

### Conclusion
This Webiste doesn't consist any Cors vulnerabiltiy

## Source
https://portswigger.net/web-security/cors
