# How HTTP Works

HTTP is a **stateless, application-level protocol** used for communication between clients and servers.

## ASCII Diagram — Request Flow
```
Client (Browser)  ──HTTP Request──▶  Server (Backend API)
Client (Browser)  ◀─HTTP Response──  Server (Backend API)
```

## HTTP Request Structure
```
GET /users HTTP/1.1
Host: api.example.com
User-Agent: Chrome
Authorization: Bearer <token>
```

## HTTP Response Structure
```
HTTP/1.1 200 OK
Content-Type: application/json

{"id":1, "name":"Victor"}
```

## Key Concepts
- Stateless  
- Supports multiple methods (GET, POST, PUT, DELETE, PATCH)  
- Uses headers for metadata  
- Uses status codes for standardized responses  

