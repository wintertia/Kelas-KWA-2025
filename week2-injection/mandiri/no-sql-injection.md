# No Sql Injection
https://play.picoctf.org/practice/challenge/443

> Can you try to get access to this website to get the flag?

## Steps

1. Given a login page, look at how it sends the request
![alt text](<images/Screenshot 2025-09-10 135325.png>)

2. Based on the given source code and title clue, use NoSQL injection and payloads from https://swisskyrepo.github.io/PayloadsAllTheThings/NoSQL%20Injection/#authentication-bypass, and don't forget to use escape characters to properly input `{\"$ne\": null}` into the fields
![alt text](<images/Screenshot 2025-09-10 135509.png>)

3. Translate the obtained token from Base64 using CyberChef for the flag
![alt text](<images/Screenshot 2025-09-10 135558.png>)