# How HTTPS Works

HTTPS = HTTP + TLS encryption.  
It ensures **confidentiality, integrity, and authentication**.

## ASCII Diagram — TLS Handshake (Simplified)
```
Client                          Server
  │       ClientHello             │
  ├──────────────────────────────>│
  │       ServerHello + Cert      │
  │<──────────────────────────────┤
  │   Validate Certificate (CA)   │
  │   Generate Session Key        │
  ├──────────────────────────────>│
Secure Encrypted Connection Established
```

## What HTTPS Protects Against
- Man-in-the-middle attacks  
- Data tampering  
- Credential/token leaks  

## Why HTTPS is Required
- OAuth flows  
- JWT validation  
- Modern browser security policies  
