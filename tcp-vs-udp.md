# TCP vs UDP

## 1. Overview
TCP and UDP are transport layer protocols used to deliver data between devices. Both serve different purposes depending on application requirements.

---

## 2. TCP (Transmission Control Protocol)

### Characteristics
- Reliable (data delivery is guaranteed)  
- Connection-oriented (requires a handshake before communication)  
- Ordered delivery (data arrives in sequence)  
- Error checking and retransmission  
- Uses three-way handshake (SYN → SYN+ACK → ACK)

### When to Use
- Web communication (HTTP/HTTPS)  
- API calls  
- File transfers  
- Email services  
- Systems requiring complete and accurate data

### Weakness
- Slower due to connection setup and reliability mechanisms

---

## 3. UDP (User Datagram Protocol)

### Characteristics
- Unreliable (no guarantee of delivery)  
- Connectionless (no handshake)  
- No data ordering  
- No retransmission  
- Lower latency

### When to Use
- Video streaming  
- Voice calls (VoIP)  
- Online gaming  
- Broadcasting or multicasting  
- Real-time applications prioritizing speed

### Weakness
- Not suitable for applications requiring complete data accuracy

---

## 4. Comparison Table

| Aspect | TCP | UDP |
|--------|-----|------|
| Connection | Yes (connection-oriented) | No (connectionless) |
| Speed | Slower | Faster |
| Reliability | High | Low |
| Order | Ensured | Not ensured |
| Overhead | Higher | Lower |
| Use case | Web, API, downloads | Streaming, gaming, real-time |

---

## 5. Summary
- **TCP** is recommended when data integrity and reliability are required.  
- **UDP** is recommended when speed and low latency are the priority.  
- The choice between TCP and UDP depends on the application's functional requirements.

