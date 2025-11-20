# HTTP in Detail — Notes

## What HTTP Is
HTTP (HyperText Transfer Protocol) is the application-layer protocol that defines:
- how clients send requests
- how servers send responses
- how browsers, APIs, and tools like curl communicate

---

## HTTP Request Structure
A request has:
- **Method** (GET, POST, etc.)
- **Path/URL**
- **Version**
- **Headers**
- **Optional Body** (POST/PUT/PATCH)

Example:
GET /index.html HTTP/1.1
Host: example.com
User-Agent: curl/7.68.0
Accept: */*

---

## HTTP Response Structure
A response has:
- **Status line** (status code + message)
- **Headers**
- **Body**

Example:
HTTP/1.1 200 OK
Content-Type: text/html
Content-Length: 1265

---

## Notes From TryHackMe Room
Write your room notes here:

- 
- 
