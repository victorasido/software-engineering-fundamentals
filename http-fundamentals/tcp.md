# Transmission Control Protocol (TCP)

TCP is a **reliable, ordered, connection-oriented** transport protocol used by HTTP.  
It ensures data arrives correctly and in order.


```
Client                        Server
  │        SYN                 │
  ├───────────────────────────>│
  │       SYN + ACK            │
  │<───────────────────────────┤
  │          ACK               │
  ├───────────────────────────>│
Connection Established
```

## Key Characteristics
- Guarantees packet delivery  
- Ensures proper ordering  
- Retransmits lost packets  
- Establishes a stable connection before sending data  

## Why HTTP Uses TCP
- Web pages require complete, ordered data  
- Prevents corruption of resources (HTML, CSS, JSON)  
