Answers:

* curl http://curlingfun:8080
* curl -k <https://curlingfun:9090/>
* curl -k -X POST <https://curlingfun:9090/> -d "skip=alabaster"
* curl -k -X GET <https://curlingfun:9090/> -H "Cookie: end=3"
* curl -k -I <https://curlingfun:9090/>
* curl -k -H "Stone: Granite" <https://curlingfun:9090/>
* curl -k --path-as-is '<https://curlingfun:9090/../../etc/hacks>'

  \


For Gold Medal/Hard Mode:

Prefer to skip ahead without guidance?  Use curl to craft a request meeting these requirements:

* HTTP POST request to <https://curlingfun:9090/>
* Parameter "skip" set to "bow"
* Cookie "end" set to "10"
* Header "Hack" set to "12ft"


To meet the requirements, you can use the following curl command:


curl -k -X POST https://curlingfun:9090/ -d "skip=bow" -H "Cookie: end=10" -H "Hack: 12ft"
Explanation:
\-k: Bypasses SSL certificate validation.
\-X POST: Specifies the HTTP POST method.
\-d "skip=bow": Sets the POST parameter skip to bow.
\-H "Cookie: end=10": Sends a cookie named end with a value of 10.
\-H "Hack: 12ft": Adds a custom HTTP header Hack with a value of 12ft.


Excellent!  Now, use curl to access this URL: <https://curlingfun:9090/../../etc/button>


To access the URL `https://curlingfun:9090/../../etc/button` without URL normalization, use the `--path-as-is`option with `curl`:

```javascript
bashCopy codecurl -k --path-as-is 'https://curlingfun:9090/../../etc/button'
```

### Explanation:

* `--path-as-is`: Prevents `curl` from modifying the URL by skipping normalization of paths like `../`.
* `-k`: Bypasses SSL/TLS certificate validation.
* Single quotes ensure the shell doesn’t interpret special characters in the URL.


Great! Finally, use curl to access the page that this URL redirects to: https://curlingfun:9090/GoodSportsmanship


To follow the redirect from `https://curlingfun:9090/GoodSportsmanship`, use the `-L` option with `curl`, which tells it to follow redirects:

```javascript
bashCopy codecurl -k -L https://curlingfun:9090/GoodSportsmanship
```

### Explanation:

* `-k`: Bypasses SSL/TLS certificate validation.
* `-L`: Instructs `curl` to follow any HTTP redirections.

This will retrieve the final page after following the redirect. Let me know if you need further details!






