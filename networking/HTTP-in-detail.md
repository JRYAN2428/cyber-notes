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


