# 🚀 First Wireshark Capture and Analysis

## 🎯 Goal
This lab demonstrates the basics of Wireshark:
- Capturing live network traffic  
- Applying display filters  
- Identifying TCP, UDP, and ICMP packets  
- Analyzing a simple ping and HTTP request flow  

---

## 🛠 Tools
- **Wireshark** (latest version)  
- **Ubuntu VM** (or any OS with network connectivity)  
- Internet access for generating traffic  

---

## 🔹 Steps

### 1. Start the Capture
- Opened Wireshark  
- Selected my network interface (`NAT` for Ethernet on my host)  
- Clicked **Start Capturing Packets**  

---

### 2. Apply Filters
Used some basic filters:
- `http` → show only HTTP traffic  
- `tcp` → show TCP packets  
- `udp` → show UDP packets  
- `ip.addr == 8.8.8.8` → show traffic to/from Google DNS  

---

### 3. Generate Test Traffic
- Ran a `ping 8.8.8.8` in the terminal → created ICMP traffic  
- Opened `http://example.com` in the browser → created DNS + TCP + HTTP traffic  

---

### 4. Analysis
- **ICMP packets** clearly visible for the ping test  
- For `example.com`:  
  - **DNS query  
  - **TCP 3-way handshake (SYN, SYN/ACK, ACK)
  - **HTTP GET request


---

### 5. Key Takeaways
- Understood how a TCP connection is established  
- Saw the real flow: **DNS → TCP → HTTP**  
- Wireshark is excellent for visualizing theoretical networking concepts  

---

## 📂 Repository Contents
- `README.md` (this file)  
- `wireshark_first_capture.pcapng` (saved capture file)  

---

## ✍️ Blog Post
I also wrote a Medium article about this lab:  
👉 [*“My First Wireshark Capture: From Ping to HTTP”*  ](https://medium.com/@itkarpathy/my-first-wireshark-capture-from-ping-to-http-a-beginners-journey-into-network-traffic-analysis-1b7ef3037d83)

---

## ✅ Next Steps
- Explore SSL/TLS handshakes  
- Try filtering by `tcp.port == 443` for HTTPS  
- Capture SSH traffic for deeper protocol analysis
- Nmap port scan

---

