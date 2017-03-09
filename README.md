# captcha-cookies
Extracting Gmail Cookies From Google Captcha

### Fast Method (using EditThisCookie extension)

Login to gmail, go to Edit This Cookie and click Export

Either keep all cookies or remove ones where the domain isn't ".google.com"

To use these cookies you need to edit them:

* Change `domain` to `url`
* If `secure=true` prefix url with `https://`, if false prefix with `http://`
* if url starts with `.`, prefix with `www` 

### Creating a cookie array for splash-party

* Login to GMail
* Go to an Adidas page with captcha (or any page on any site with a google captcha)
* Go into browser developer tools, select "Application", then "Cookies"
* Go to the cookies under "https://www.google.com"
* For each one of those cookies, create an object like the following, inside an array

##This is extremely important:
Make sure to use secure: true when needed, and httpOnly: true when needed
You'll see each cookie has that value true or false in chrome

```
            {
                "url": "https://www.google.com",
                "name": "<cookiename>",
                "value": "<cookievalue>",
                "path": "/",
                "secure": true

            }
```

The complete Array should look like this

```
[
            {
                "url": "https://www.google.com",
                "name": "abc",
                "value": "123",
                "path": "/",
                "secure": true

            },
                        {
                "url": "https://www.google.com",
                "name": "fdsd",
                "value": "gfdg",
                "path": "/",
                "secure": false,
                "httpOnly": true

            },
                        {
                "url": "https://www.google.com",
                "name": "y56g",
                "value": "sdffd",
                "path": "/",
                "secure": true

            }
]

```


set that array as `gCookies` in the splash-party config
