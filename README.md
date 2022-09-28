# Some tips for bot developers.

# Why you should not use the popular python requests module
<li>The first reason is that it is slow</li>
<li>Requests is a great module, but if you want to create a bot such as a account generator then i would recommend (httpx)[https://github.com/encode/httpx], why httpx? well requests isn't good for automating tasks, the reason for that is that it is detected due to its TLS config. The second reason is that httpx is generelly faster then requests and it also supports async</li>

# If you are using httpx or requests or any other http clients, please use sessions/clients
<li>Clients/Sessions are gennerly faster then regular requests.get/post, lemme explain, when ever you call a requests.get/post it creates a session, makes a request to the target server then immediately closes the session, however with sessions the connection is cached for later use.</li>
<li>Cookie persistence, http clients like httpx do all the work for you, for expample if you make a request to `example.com` and it sets the cookie you would first have to get the cookie, store it somewhere then use it in your other request, however with cookie persistence you dont have to do that, all the work is done by the http client for you, you just have to make the request and it will save the cookies set by the server and use it in later requests.</li>

# What browser framework should you use and what language should i code my bot that uses browsers?
<li>JS is the best language in my POV if you want to make a scrapping bot using browsers.</li>
<li>For bots you should use puppeteer or playwright with (puppeteer/playwright-extra)[https://github.com/berstend/puppeteer-extra] with puppeteer-extra-plugin-stealth for super low bot detection.</li>
<li>Use packages like [Ghost Cursor](https://github.com/Xetera/ghost-cursor) to make human-like mouse movements .</li>

# TLS Fingerprinting(JA3)

## What site should i use to get my browser's JA3?

https://tls.peet.ws/api/clean you can use this url to get your ja3 fingerprint as well as your akamai fingerprint

## How do i "spoof" ja3?

Spoofing JA3 can be challenging, if you want something easy to use you can use (CycleTLS)[https://github.com/Danny-Dasilva/CycleTLS]

