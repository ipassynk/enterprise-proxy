# enterprise-proxy


How to set-up proxy in enterprise for npm, git, bower, tsd, typings...
I am thing to make a script to general it and update password... (TODO)

##Replace
*user* with your enterpise username
*password* with your enterpise password
*hostname:port*  with enterpise proxy hostname:port


* http proxy
```
set HTTP_PROXY=http://user:password@hostname:port
set HTTPS_PROXY=http://user:password@hostname:port
```

* Git (if you have it)
```
git config --global http.proxy %HTTP_PROXY%
git config --global https.proxy %HTTPS_PROXY%
git config --global http.sslVerify false
```

* npm. Create .npmrc file in you user home with the folloiwng content
```
https-proxy=http://user:password@hostname:port
proxy=http://user:password@hostname:port
strict-ssl=false
rejectUnauthorized=false
```

* bower. Create .bowerrc file in you user home with the folloiwng content
```
{
    "https-proxy": "http://user:password@hostname:port",
    "proxy": "http://user:password@hostname:port",
    "strict-ssl": false,
    "rejectUnauthorized": false
}
```

* tsd. Create .tsdrc file in you user home with the folloiwng content
```
{
    "https-proxy": "http://user:password@hostname:port",
    "proxy": "http://user:password@hostname:port",
    "strictSSL": false,
    "rejectUnauthorized": false
}
```

* typings. Create .tsdrc file in you user home with the folloiwng content
```
{
    "https-proxy": "http://user:password@hostname:port",
    "proxy": "http://user:password@hostname:port",
    "strictSSL": false,
    "rejectUnauthorized": false
}
```

Enjoy!

---
Julia Passynkova
