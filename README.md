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
git config --global url."https://".insteadOf git://
```

* npm. Create .npmrc file in you user home directory with the folloiwng content
```
https-proxy=http://user:password@hostname:port
proxy=http://user:password@hostname:port
strict-ssl=false
rejectUnauthorized=false
```

* bower. Create .bowerrc file in you user home directory with the folloiwng content
```
{
    "https-proxy": "http://user:password@hostname:port",
    "proxy": "http://user:password@hostname:port",
    "strict-ssl": false,
    "rejectUnauthorized": false
}
```

* tsd. Create .tsdrc file in you user home directory with the folloiwng content
```
{
    "https-proxy": "http://user:password@hostname:port",
    "proxy": "http://user:password@hostname:port",
    "strictSSL": false,
    "rejectUnauthorized": false
}
```

* typings. Create .tsdrc file in you user home directory with the folloiwng content
```
{
    "https-proxy": "http://user:password@hostname:port",
    "proxy": "http://user:password@hostname:port",
    "strictSSL": false,
    "rejectUnauthorized": false
}
```

### C++ installation
Some of the required npm packages use [node-gyp](https://github.com/nodejs/node-gyp) to compile native C++ dll. 
It is required to install C++ compiler and python for node-gyp.

I had to install Visual Studio 2015
Please read [Microsoft Prerequisites](https://github.com/Microsoft/nodejs-guidelines/blob/master/windows-environment.md#prerequisites)
It is important to select 'Custom->Programming Languages->Visual C++->Common Tools for Visual C++' during installation

Use https://www.microsoft.com/en-us/download/details.aspx?id=48146 to download vs_community.exe

Enjoy!

---
Julia Passynkova
