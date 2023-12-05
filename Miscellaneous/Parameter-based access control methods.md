
Some applications determine the user's access rights or role at login, and then store this information in a user-controllable location. This could be:

- A hidden field.
- A cookie.
- A preset query string parameter.

The application makes access control decisions based on the submitted value. For example:

`https://insecure-website.com/login/home.jsp?admin=true https://insecure-website.com/login/home.jsp?role=1`

This approach is insecure because a user can modify the value and access functionality they're not authorized to, such as administrative functions.

In the next lab:

This lab has an admin panel at `/admin`, which identifies administrators using a forgeable cookie.

So we just intercept the request with burpsuite, and change the cookie to Admin=True

POST /login HTTP/2
Host: 0aa600a904febdec8088ad8d00b80094.web-security-academy.net
Cookie: Admin=false; session=a8WA9XxcAgZfFxBCE6YeHeJBX3pMNmAM

Now we are an admin user