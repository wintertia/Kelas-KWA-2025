# More SQLi
https://play.picoctf.org/practice/challenge/358

> Can you find the flag on this website.

## Steps

1. Try classic SQLite `' or 1=1--` injection but fail because the password select goes before username
![alt text](<images/Screenshot 2025-09-10 142147.png>)
![alt text](<images/Screenshot 2025-09-10 142153.png>)

2. Flip the injection around and successfully login to a table with a search feature with 3 columns
![alt text](<images/Screenshot 2025-09-10 142441.png>)
![alt text](<images/Screenshot 2025-09-10 143908.png>)

3. Use SQL union injection for 3 columns to leak information from sqlite_master `' union select name,sql,3 from sqlite_master;--`
![alt text](<images/Screenshot 2025-09-10 143840.png>)

4. Flag found in the `more_table` table so select it using another SQL union injection `' union select flag,2,3 from more_table;--`
![alt text](<images/Screenshot 2025-09-10 143829.png>)
