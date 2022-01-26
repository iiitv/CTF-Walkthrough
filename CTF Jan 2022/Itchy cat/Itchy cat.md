# Itchy cat - Web Exploitation

## Link to the Question

[Click here](https://jhlm.herokuapp.com/)


## Answer

```
`flag{itsallaboutthespecialeffects}`
```

## Solution

When we try to visit the site, we automatically get redirected to the login page.

The question description is `Injection hurts cat too`, so we can try to inject a SQL query to get the flag.

As we don't know the username, we try username `admin`. If this doesn't work, we try `root`.

We can guess the sql query be something like `SELECT * FROM users WHERE username = "username" AND password = "password"`.

So we will send password `" OR 1=1 OR "` to the login page. so the final query is `SELECT * FROM users WHERE username = "admin" AND password = "" OR 1=1 OR ""`.

And we are successfully logged in, and the response is
```text
Hello admin
flag: flag{itsallaboutthespecialeffects}
```

So the flag is `flag{itsallaboutthespecialeffects}`.
