# Ephemeral Accountant

> Log in with the (non-existing) accountant acc0unt4nt@juice-sh.op without ever registering that user.

## Steps

1. Figure out how the login query works with Burpsuite
![alt text](<images/Screenshot 2025-09-10 075327.png>)

2. Use SQL Injection to manipulate the User table with a temporary account
![alt text](<images/Screenshot 2025-09-10 075421.png>)
![alt text](<images/Screenshot 2025-09-10 075457.png>)