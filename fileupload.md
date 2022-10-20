# What is file upload vulnerability ?

File upload vulnerabilities are when a web server allows users to upload files to its filesystem without sufficiently validating things like their name, type, contents, or size. Failing to properly enforce restrictions on these could mean that even a basic image upload function can be used to upload arbitrary and potentially dangerous files instead. This could even include server-side script files that enable remote code execution

![image](https://user-images.githubusercontent.com/72333625/197034706-e8877f31-1d49-41a8-9e56-ec3e2c6b3441.png)

# What is the impact of file upload vulnerabilities ?

The impact of file upload vulnerabilities generally depends on two key factors:

-> Which aspect of the file the website fails to validate properly, whether that be its size, type, contents, and so on.

-> What restrictions are imposed on the file once it has been successfully uploaded.

# Things tried on the website for the vulnerability 

1. First tried to upload a simple jpeg file on this directory (/Home/UploadImage)
2. Message got (Access to the path 'E:\Inetpub\vhosts\TeqCraft.com\Magnus.jalatechnologies.com\Uploads\128\' is denied.
Error!)
3. From this message we get to know that no type of file can be uploaded
4. File type used to upload (jpg, jpeg , png )

# Conclusions

The given website is safe from file upload vulnerability because the website doesn't give any kind of permission to user or guests to upload any file .
