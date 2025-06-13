`SQL injection 
- This type of vulnerability arises from the unsafe handling of user-supplied input. 

For more: [[SQL Injection]]

`File Inclusion
- Reading source code to find a hidden page or directory which exposes additional functionality that can be used to gain remote code execution.

`Unrestricted File Upload`
- A web application that allows a user to upload a profile picture that allows any file type to be uploaded (not just images). This can be leveraged to gain full control of the web application server by uploading malicious code.

`Insecure Direct Object Referencing (IDOR)
- When combined with a flaw such as broken access control, this can often be used to access another user's files or functionality. An example would be editing your user profile browsing to a page such as /user/701/edit-profile. If we can change the `701` to `702`, we may edit another user's profile!

`Broken Access Control
- Another example is an application that allows a user to register a new account. If the account registration functionality is designed poorly, a user may perform privilege escalation when registering. Consider the `POST`request when registering a new user, which submits the data `username=bjones&password=Welcome1&email=bjones@inlanefreight.local&roleid=3`. What if we can manipulate the `roleid` parameter and change it to `0` or `1`. We have seen real-world applications where this was t


