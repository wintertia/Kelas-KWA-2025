# Login Admin

> Log in with the administrator's user account.

## Steps

1. Try basic SQL injection payload `' or 1=1--` to bypass having to input password.
![input](<images/Screenshot 2025-09-10 072512.png>)

2. No email checks meaning it defaults to id 1 which is usually the admin.
![win](<images/Screenshot 2025-09-10 072525.png>)