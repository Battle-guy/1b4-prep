- Example Questions and filters to practice
These questions should cover basic filtering within wireshark
### **1. How many packets use TCP?**  
**Filter:** `tcp`

---

### **2. How many packets use UDP?**  
**Filter:** `udp`

---

### **3. How many packets are ARP requests?**  
**Filter:** `arp.opcode == 1`

---

### **4. How many packets are ARP replies?**  
**Filter:** `arp.opcode == 2`

---

### **5. What packets contain the first completed SYN‑ACK?**  
**Filter:** `tcp.flags.syn == 1 && tcp.flags.ack == 1`

---

### **6. What is the first DNS query sent by the host?**  
**Filter:** `dns && dns.flags.response == 0`

---

### **7. What IP addresses does the host communicate with?**  
**Filter:** `ip.addr == <host IP>`  
*(Students replace `<host IP>` with the source IP they find.)*

---

### **8. How many HTTP GET requests are in the capture?**  
**Filter:** `http.request.method == "GET"`

---

### **9. How many HTTP POST requests are in the capture?**  
**Filter:** `http.request.method == "POST"`

---

### **10. What is the largest packet in the capture?**  
**Filter:** `frame.len`  
*(Sort by length.)*

---

### **11. Which packets contain TLS Client Hello messages?**  
**Filter:** `tls.handshake.type == 1`

---

### **12. Which packets contain TLS Server Hello messages?**  
**Filter:** `tls.handshake.type == 2`

---

### **13. How many ICMP echo requests were sent?**  
**Filter:** `icmp.type == 8`

---

### **14. How many ICMP echo replies were received?**  
**Filter:** `icmp.type == 0`

---

### **15. Which packets show TCP retransmissions?**  
**Filter:** `tcp.analysis.retransmission`

---

### **16. Which packets show TCP duplicate ACKs?**  
**Filter:** `tcp.analysis.duplicate_ack`

---

### **17. What DNS server IP addresses are being queried?**  
**Filter:** `dns && dns.flags.response == 0`  
*(Sort by destination.)*

---

### **18. Which packets contain HTTP objects that can be exported?**  
**Filter:** `http && http.content_type`

---

### **19. What packets show a TCP connection being reset?**  
**Filter:** `tcp.flags.reset == 1`

---

### **20. What packets show the completion of the TCP three‑way handshake?**  
**Filters:**  
- SYN: `tcp.flags.syn == 1 && tcp.flags.ack == 0`  
- SYN‑ACK: `tcp.flags.syn == 1 && tcp.flags.ack == 1`  
- ACK: `tcp.flags.ack == 1 && tcp.len == 0`

---

If you want, I can turn these into:

- a **full quiz**,  
- a **lab worksheet**,  
- or a **complete Wireshark training module** with answer keys and explanations.

Just tell me the format you want.
