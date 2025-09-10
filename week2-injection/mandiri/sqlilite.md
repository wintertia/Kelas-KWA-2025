# SQLiLite
https://play.picoctf.org/practice/challenge/304

> Can you login to this website?

## Steps

1. Based on the challenge title, I can guess it's an SQLite injection, and based on classic SQL injection payloads i used `' or 1=1--` for the username and leaving the password with anything
![alt text](<images/Screenshot 2025-09-10 141725.png>)

2. Reveal the flag with inspect element
![alt text](<images/Screenshot 2025-09-10 141749.png>)
