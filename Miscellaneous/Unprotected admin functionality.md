
We got this link:
https://0aec00bf03e53b9182f1200700bd0009.web-security-academy.net/

Now we can check for:
https://0aec00bf03e53b9182f1200700bd0009.web-security-academy.net/robots.txt

and there we find /administrator-panel/ which means is not indexed by search engines

Now we can access the admin panel and delete users.

Sometimes is hidden, but we can still find something in the code just like that:

```
<script>
var isAdmin = false;
if (isAdmin) {
   var topLinksTag = document.getElementsByClassName("top-links")[0];
   var adminPanelTag = document.createElement('a');
   adminPanelTag.setAttribute('href', '/admin-5vitvy');
   adminPanelTag.innerText = 'Admin panel';
   topLinksTag.append(adminPanelTag);
   var pTag = document.createElement('p');
   pTag.innerText = '|';
   topLinksTag.appendChild(pTag);
}
</script>
```

So we found /admin-5vitvy
