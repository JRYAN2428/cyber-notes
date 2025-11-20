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
