Module 6 : How The Web Works :

DNS in Detail:
--------------
DNS (Domain Name System)
provides a simple way for us to communicate with devices on the internet without remembering complex numbers.
*Domain Hierarchy:
-------------------
1- TLD (Top-Level Domain):
ex:
the tryhackme.com TLD is .com. 
* There are two types of TLD, gTLD (Generic Top Level) and ccTLD (Country Code Top Level Domain)
* a gTLD was meant to tell the user the domain name's purpose:
  com ---->commercial
  org ---->organisation
  edu ----->education
  gov ------>government
* a ccTLD was used for geographical purposes:
* ca---->Canada
* .co.uk-----> United Kingdom
* on. Due-------> demand
* 

2-Second-Level Domain:
 tryhackme is the Second Level Domain. 
 *the second-level domain is limited to 63 characters + the TLD and can only use a-z 0-9 and hyphens (cannot start or end with hyphens or have consecutive hyphens).
 
3-Subdomain:
 in the name admin.tryhackme.com the admin part is the subdomain.
You can use multiple subdomains split with periods to create longer names, such as jupiter.servers.tryhackme.com. But the length must be kept to 253 characters or less. There is no limit to the number of subdomains you can create for your domain name.
------------------------
DNS Record Types 
A Record → points to an IPv4 address.
AAAA Record → points to an IPv6 address.
CNAME Record → points to another domain name.
MX Record → specifies the mail servers for a domain.
TXT Record → stores text information, often used for verification and email security.
-----------------------------
What happens when you make dns  a request
DNS Lookup — Short Summary

Computer → Recursive DNS → Root Server → TLD Server → Authoritative DNS → IP Address

Computer: Checks local cache first.
Recursive DNS: Searches its cache; if not found, asks other DNS servers.
Root Server: Directs the request to the correct TLD server.
TLD Server: Finds the authoritative nameserver.
Authoritative DNS: Provides the correct DNS record/IP.
TTL: Determines how long the result is cached.
-------------------------------------------------------------------------------
HTTP in Detail:
----------------
http:HyperText Transfer Protocol
 HTTP is the set of rules used for communicating with web servers for the transmitting of webpage data, whether that is HTML, Images, Videos, etc.
 HTTPS? (HyperText Transfer Protocol Secure)
 HTTPS is the secure version of HTTP
 HTTPS data is encrypted so it not only stops people from seeing the data you are receiving and sending, but it also gives you assurances that you're talking to the correct web server and not something impersonating it.
 
  What is a URL? (Uniform Resource Locator)
  Scheme: This instructs on what protocol to use for accessing the resource such as http  , HTTPS,ftp (File Transfer Protocol).
  User: Some services require authentication to log in, you can put a username and password into the URL to log in.
  Host: The domain name or IP address of the server you wish to access.
  Port: The Port that you are going to connect to, usually 80 for HTTP and 443 for HTTPS, but this can be hosted on any port between 1 - 65535.
  Path: The file name or location of the resource you are trying to access.
  Query String: Extra bits of information that can be sent to the requested path. For example, /blog?id=1 would tell the blog path that you wish to receive the blog article with the id of 1.
  Fragment: This is a reference to a location on the actual page requested. This is commonly used for pages with long content and can have a certain part of the page directly linked to it, so it is viewable to the user as soon as they access the page.
  
  Request:

GET → What I want → Who I am → Where I came from

Response:

Status → Server → Date → Content Type → Content Length → Content

-------------------------------
HTTP Methods:
GET = Read
POST = Create
PUT = Update
DELETE = Delete
-------------
http Status Codes:
100-199 - Information Response 	These are sent to tell the client the first part reset  of their request has been accepted and they should continue sending the of their request. These codes are no longer very common.
200-299 - Success 	This range of status codes is used to tell the client their request was successful.
300-399 - Redirection 	These are used to redirect the client's request to another resource. This can be either to a different webpage or a different website altogether.
400-499 - Client Errors 	Used to inform the client that there was an error with their request.
500-599 - Server Errors 	This is reserved for errors happening on the server-side and usually indicate quite a major problem with the server handling the request.
--------------------------------
200 - OK 	The request was completed successfully.
201 - Created 	A resource has been created (for example a new user or new blog post).
301 - Moved Permanently 	This redirects the client's browser to a new webpage or tells search engines that the page has moved somewhere else and to look there instead.
302 - Found 	Similar to the above permanent redirect, but as the name suggests, this is only a temporary change and it may change again in the near future.
400 - Bad Request 	This tells the browser that something was either wrong or missing in their request. This could sometimes be used if the web server resource that is being requested expected a certain parameter that the client didn't send.
401 - Not Authorised 	You are not currently allowed to view this resource until you have authorised with the web application, most commonly with a username and password.
403 - Forbidden 	You do not have permission to view this resource whether you are logged in or not.
405 - Method Not Allowed 	The resource does not allow this method request, for example, you send a GET request to the resource /create-account when it was expecting a POST request instead.
404 - Page Not Found 	The page/resource you requested does not exist.
500 - Internal Service Error 	The server has encountered some kind of error with your request that it doesn't know how to handle properly.
503 - Service Unavailable 	

This server cannot handle your request as it's either overloaded or down for maintenance.



Common Request Headers


Request:

Host = Which website
User-Agent = Which browser
Content-Length = How much data
Accept-Encoding = Which compression
Cookie = Remember me

Common Response Headers
Response:

Set-Cookie = Save this cookie
Cache-Control = Cache for how long
Content-Type = What type of data
Content-Encoding = How data is compressed



-------------
Cookies:
------
Cookie = small piece of data stored in your browser/computer.
Set-Cookie saves the cookie, Cookie sends it back.
Set-Cookie = Server → Browser
Cookie = Browser → Server
-----------------------------
How Websites Work:
-------------------
By the end of this room, you'll know how websites are created and will be introduced to some basic security issues.
Front End (Client-Side) - the way your browser renders a website.
Back End (Server-Side) - a server that processes your request and returns a response


1. inject HTML

Putting It All Together:
Load Balancers
Load Balancer = distributes traffic between servers + provides failover.

Health Check = checks if the server is alive/working




CDN (Content Delivery Networks)
CDN = stores static files on servers around the world and delivers them from the nearest server.

CDN → Faster website + Less traffic on the main server


Databases
 You'll come across some common databases: MySQL, MSSQL, MongoDB, Postgres, and more; 


WAF (Web Application firewall)
WAF = protects the web server by inspecting and blocking malicious requests.


How Web servers work:
-------------------
Web Server → receives HTTP requests and delivers web content.
Virtual Host → allows multiple websites on one server.
Static Content → content that doesn't change.
Dynamic Content → content that can change depending on the request.
Frontend → what the user sees.
Backend → what happens behind the scenes.
Backend languages → PHP, Python, Ruby, NodeJS, etc.


--------------
1- request tryhackme.com in your browser
2-check local cache for ip address
3-check your recursive dns server for address
4-query root server to find authoritative dns srver
5-authoritative dns server advises the ip address for the website
6-request passes through a web application firewall
7-request passes through a load balancer
8-connect to webserver on port 80 or 443
9-web server receives the get request
10-web application talks to database
11-your browser render the html into a viewable website

13

