# User Credentials

> Retrieve a list of all user credentials via SQL Injection.

Steps

1. Try and find out important columns in the user table by using SQL injection on the login page, we see id, email, and password hash
![alt text](<images/Screenshot 2025-09-10 081159.png>)

2. Use the search query SQL Injection Union to leak the user table
![alt text](<images/Screenshot 2025-09-10 081047.png>)
