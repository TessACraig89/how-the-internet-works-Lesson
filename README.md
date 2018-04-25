# Install Fest!
Go here and follow the instructions! https://git.generalassemb.ly/WDIplus-ATX/installfest

# How the Internet works

### Objectives

*After this lesson, students will be able to:*

- Explain the differences between a client and server
- Explain the difference between the Internet and the World Wide Web
- Explain the significance of an Internet Protocol (IP) address
- Explain how data travels through the internet
- Breakdown the components of a URL: protocol, subdomain, domain, extension, resources
- Identify and describe the most common HTTP request/response headers and the information associated with each

### Preparation
*Before this lesson, students should already be able to:*

- Use a web browser

## Intro - Server, Client, Request, HTTP 

The internet as you know comes down to requests and responses - you send information out to the web, and based on the info you send, you get information back.

#### HTTP 101

HTTP stands for "Hyper Text Transfer Protocol" - because it's a protocol for computers to exchange information via internet infrastructure.

- **Host** - a computer or other device connected to a computer network; host may offer information resources, services, and applications (via computer code!) to users or other computers on the network
  - Ex: servers and web services
- **Client** - the requesting program in the client/host relationship; the client initiates an HTTP request message, which is serviced through a HTTP response message in return
  - Ex: browsers, terminals, SQL clients

![](https://cdn.tutsplus.com/net/authors/jeremymcpeak/http1-request-response.png)

#### Servers have addresses, called an IP address

```
123.123.123.123
```

#### Domain Registrars map URLs to IP addresses for user-friendliness 

| Domain Name  | IP Address    |
|--------------|---------------|
| apple.com    | 17.172.224.47 |
| facebook.com | 31.13.65.1    |
| google.com   | 216.58.192.46 |

We can put IP addresses into our browswer if we want!

#### What happens when you go to google.com? A 10,000 foot view

1. Your browser makes an HTTP request, a GET request specifically to Google.com
1. This gets mapped to a IP address
1. Routers 'route' your request to the physical computer at that IP address
1. Google processes the request and creates a response containing HTML, CSS, and JS
1. Google sends that response back to YOUR IP address, which is in the header of your request
1. Your browser renders the web page on the screen. 

## Internet vs Web

- Discuss your thoughts on the difference with a partner: 3 min.

<details>
<summary>What's the difference?</summary>
<br>
	
1. The Internet is the network of all of the interconnected computers in the world!
	
1. The World Wide Web is a massive collection of HTML pages, along with CSS and JS that can be used in the browser. 

1. The Internet **contains** the World Wide Web.
</details>
	
<br>
	
<details>
<summary>What are some examples of things that are part of the internet but not the WWW? Slack me your ideas!</summary>
<br>
	
1. Torrents
	
1. Email

1. SMS

1. Usenet
</details>

#### Anatomy of a URL or Uniform Resource Locator


```
    http://www.example.org/hello/world/foo.html?foo=bar&baz=bat#footer
    \___/  \_____________/ \__________________/ \_____________/ \____/
  protocol  host/domain name        path         querystring     hash/fragment
```

Element | About
------|--------
protocol | the most popular application protocol used on the world wide web is HTTP. Other familiar types of application protocols include FTP, SSH, HTTPS
host/domain name | the host or domain name is looked up in DNS to find the IP address of the host - the server that's providing the resource
path | web servers can organise resources into what is effectively files in directories; the path indicates to the server which file from which directory the client wants
querystring | the client can pass parameters to the server through the querystring (in a GET request method); the server can then use these to customise the response - such as values to filter a search result
hash/fragment | the URI fragment is generally used by the client to identify some portion of the content in the response; interestingly, a broken hash will not break the whole link - it isn't the case for the previous elements

<br>
_The Schema above is from [Tuts +](http://code.tutsplus.com/tutorials/http-the-protocol-every-web-developer-must-know-part-1--net-31177)_


## Responses and HTTP Status Codes

When a server creates a response, a header is generated just like a request. In that header is a status code that contains the status of the response. You will be familliar with the dreaded 404, not found! status. 

All are 3 digit numbers that start with a 1, 2, 3, 4 or 5

- 1xx Informational
- 2xx Success
- 3xx Redirection
- 4xx Client Error
- 5xx Server Error

Since HTTP is a text-based protocol, it’s easy to make HTTP requests manually

```bash
curl https://www.reddit.com/r/holofractal
```

_Some text taken from [One Month](http://learn.onemonth.com/understanding-http-basics)_

#### Server-side vs. Client-side

**The Client** is kind of like the **user**. Usually it is a person using a browser. But not always! Sometimes the client is just some code that makes requests for traffic automatically every 5 minutes, or a bot that posts warm and fuzzy compliments to twitter! Point being: **The client is the thing that makes the request**. For most of this course, this is done through a browser. If there is computer code involved on the browser side, it can only be JavaScript. JavaScript was designed to run in a browser. Browsers are made only to run JavaScript. 

**The Server** has requests made of it. It processes requests, handles business logic, stores things in a database, and sends responses. A server is just a computer somewhere, probably with no screen, keyboard or mouse. Since a server is just a computer, any sort of code can be run on it. Python, Ruby, C, Java, and since 2009, JavaScript. 

## Review of Internet Fundamentals - Independent Practice

Answer and discuss the following questions with a partner:

- What does HTTP stand for?
- Compare different HTTP status codes.
- Draw your own diagram of a request/response cycle and label where the following would come into play: client, host/server, URL, client-side languages, server-side languages, data, router

![](http://i.giphy.com/eoxomXXVL2S0E.gif)
