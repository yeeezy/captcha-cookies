# captcha-cookies
Extracting Gmail Cookies From Google Captcha


### Creating a cookie array for splash-party

* Login to GMail
* Go to an Adidas page with captcha
* Go into browser developer tools, select "Application", then "Cookies"
* Go to the cookies under "https://google.com"
* For each one of those cookies, create an object like the following, inside an array

```
            {
                url: "https://www.google.com",
                name: "<cookiename>",
                value: "<cookievalue>",
                path: "/",
                secure: true

            }
```

The complete Array should look like this

```
[
            {
                url: "https://www.google.com",
                name: "abc",
                value: "123",
                path: "/",
                secure: true

            },
                        {
                url: "https://www.google.com",
                name: "fdsd",
                value: "gfdg",
                path: "/",
                secure: true

            },
                        {
                url: "https://www.google.com",
                name: "y56g",
                value: "sdffd",
                path: "/",
                secure: true

            }
]

```


set that array as `gCookies` in the splash-party config
