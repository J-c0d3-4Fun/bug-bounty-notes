This type of vulnerability arises from the unsafe handling of user-supplied input. 
- It can result in access to sensitive data, reading/writing files on the database server, and even remote code execution.
- Often used on webapps that require Active Directory for Authentication
	- can often pull most or all Active Directory user email addresses, which are often the same as their usernames
	- This data can then be used to perform a [password spraying](https://us-cert.cisa.gov/ncas/current-activity/2019/08/08/acsc-releases-advisory-password-spraying-attacks) attack against web portals that use Active Directory for authentication such as VPN or Microsoft Outlook Web Access/Microsoft O365

[[Flaws]]
