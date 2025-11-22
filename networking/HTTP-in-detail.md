# HTTP in detail

## What is HTTP? (HyperText Transfer Protocol)
- Used when visiting websites
- set of rules used for communicating with web servers to transmit data for webpages, and additional information like HTML, Images
    - Or even query parameters, headers, cookies, and form data
        - Additionally, authentication tokens, session IDs, and cache directives
        - HTTP can be used to pass metadata requests and responses; content types, content lengths, encoding information

## What is HTTPS? (Hypertext Transfer Protocol Secure)
- Secure version of HTTP
- Data is encrypted. People can't see the data you are recieving or sending. The encryption also insures that you are talking to the legitimate web server
    - The Secure, 'S' part of HTTPS encompasses encryption protocols such as SSL/TLS
    - SSL/TLS work by encrypting the data being transmitted between the client and server. SSL authenticates the server's identity, and establish a secure connection
    - TLS (Transport Layer Security) provides a secure channel between two endpoints. It encrypts the data transmitted. TLS works by verifieing the identity of parties involved, through certificates.

# Requests and Responses
Accessing a website requires:
- browser to make requests to the web server for assets such as HTML, Images, and download the response
- browsers need to know how, and where to locate/access these resources, which is why we use URLS to help

## What is a URL? (Uniform Resource Locator)
- URL is mainly an instruction on how to access resources on the internet
    - Sceheme: What protocol to use for accessing resources, HTTP, HTTPS, FTP
    - User: Services may require user authentication to log in, user and pass in URL
    - Host: Domain name/IP address of server
    - Port: Usually 80 for HTTP, 443 for HTTPS. Can be hosted on any port.
    - Path: Filename/location/dir
    - Query String: Additional pieces of information relevant to the associated directory, generally to attach an ID to a specific branch of information
    - Fragment: Reference to a location on the actual page requested. Used for quick access to a page with a lot of content, to fast track information processing for relevant information provided by the link in question

## Making a Request
- Typically done via "GET"
- GET /HTTP/1.1 (used to denote the version of the HTTP protocol being used)
    - Request is sent by the GET method (GET / HTTP/1.1
    -  What website we want (Host: google.com)
    -  What browser we're using (User-Agent: Mozilla/5.0 Firefox/87.0
    -  Referer: https://tryhackme.com/

# HTTP Methods

There are various methods of intention by the client:
- Get Request
    - Used for extracting information
- POST Request
    - Submitting data to a web server; potentially creating new records
- PUT Request
    - Submitting data to web server to update information
- DELETE Request
    - Deleting information and records from a web server

# HTTP Status Codes
When a HTTP responds, they respod with a status code:
- 100-199 Information Response; first part of request recieved, send rest of request (Not used much anymore)
- 200-299 Success; Tells client request was successful
- 300-399 Redirection; Used to redirect client request to different webpage/webserver
- 400-499 Client Errors; Informs client of error in request
- 500-599 Server Errors; Errors that happen on the server side (Generally a major problem for the server handling the request)

Common HTTP Status Codes:
- 200; OK
- 201; Created
- 301; Moved permanently; redirect client browser to new webpage, or tells earch engines that page moved look elsewhere
- 302; Found; Temporary change
- 400; Bad Request; Something wrong or missing in request, web server may be expecting precise parameter, or formatting that client didn't send
- 401; Not authorised: Potentially need a login or security clearance
- 403: Forbidden: No permission to view regardless
- 405; Method Not Allowed: resource doesn't allow a GET request to resource of create account which would be expecting a POST request
- 404: Page not Found: Page/resource requested does not exist
- 500; Internal Service Error: Server encountered error that it doesn't understand
- 503; Service Unavailble: Server couldn't handle request; overloaded or down

# Headers
Additional bits of data that you _can_ send to the web server when making requests

**HOST:** Web servers can host multiple websites, host headers specify the domain name of the server you're trying to reach. Client > HTTP request > Server: Domain? ?HTTP request encompasses Host Header > Send There
**User-Agent:** Browser Software & Version Number > Tells Wbeserver your browser software > helps format website for browser client; some elements of HTML, JavaScript and CSS only available in certain browsers.
**Content Length:** Sending data such as a form (POST), content length describes how much data is expected in web request; validates integrity of data
**Accept Encoding** Web server is told of compression methods applicable to browser, handle smaller amount od data over internet
**Cookie** Data sent to the server which holds information

## Common Response Headers
Client > Server > Client
**Set Cookie** Information to store content of response in browser cache
**Cache control:** Length of cache storage in browser
**Content Type** Type of data being returned; HTML, CSS, JavaScript, Images, PDF, Video. Content Type header > Browser understands how to process it
**Content Encoding:** method used to compress data to make it smaller when sending over internet



