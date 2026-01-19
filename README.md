# Task 3 – Networking Basics for Cyber Security

## Cyber Security Internship

This repository contains the complete work for **Task 3: Networking Basics for Cyber Security**.  
The task focuses on understanding basic networking concepts and analyzing live network traffic using **Wireshark**, including TCP handshake analysis, plain-text traffic detection, and encrypted HTTPS communication.

---

## Objective

- Learn basic networking concepts (IP, TCP, DNS)
- Capture live network traffic using Wireshark
- Filter packets by protocol (TCP, HTTP, DNS)
- Observe the TCP three-way handshake
- Identify plain-text vs encrypted traffic
- Understand why HTTPS is more secure than HTTP
- Analyze DNS queries

---

## Tools & Environment

- **Wireshark**
- **Python (Flask)**
- **HTML & CSS**
- **Kali Linux**
- **Loopback Interface (lo)**
- **Browser:** Firefox

---

## Project Overview

A simple **login web application** was developed using Flask to generate real network traffic.

- HTTP was used to demonstrate **plain-text credential exposure**
- HTTPS (TLS) was enabled to demonstrate **encrypted traffic**
- Wireshark was used to analyze and compare both cases

---

## Repository Structure
```bash
│
├── README.md
│
├── src/
│ ├── app.py
│ ├── cert.pem
│ ├── key.pem
│ ├── templates/
│ │ └── login.html
│ └── static/
│ └── style.css
│
├── captures/
│ ├── http_plaintext_capture.pcapng
│ └── https_encrypted_capture.pcapng
│
├── screenshots/
│ ├── tcp_three_way_handshake.png
│ ├── http_plaintext_credentials.png
│ ├── https_encrypted_traffic.png
│ └── dns_query_analysis.png
```


---

## Wireshark Analysis

### 1. TCP Three-Way Handshake

The TCP connection was established using:
1. **SYN** – Client requests connection  
2. **SYN-ACK** – Server acknowledges  
3. **ACK** – Client confirms connection  

This confirms a reliable TCP connection before data transfer.

---

### 2. HTTP (Plain-Text Traffic)

- Protocol: HTTP
- Method: POST
- Content-Type: application/x-www-form-urlencoded

**Observed in Wireshark:**
 - username=admin
 - password=admin123


**Conclusion:**  
HTTP transmits sensitive information in plain text and is insecure.

---

### 3. HTTPS (Encrypted Traffic)

- Protocol: TLS
- Payload: Encrypted Application Data
- Credentials: **Not visible**

**Conclusion:**  
HTTPS encrypts data using TLS, preventing attackers from reading sensitive information even if packets are captured.

---

### 4. DNS Analysis

DNS queries were captured and analyzed using the filter:

This shows domain name resolution before communication begins.

---

## HTTP vs HTTPS Comparison

| Feature | HTTP | HTTPS |
|------|------|------|
| Encryption | No | Yes |
| Credentials Visible | Yes | No |
| Security Level | Low | High |
| Protocol | HTTP | TLS + HTTP |

---

## Final Outcome

- Successfully analyzed live network traffic
- Observed TCP three-way handshake
- Identified plain-text credential leakage
- Verified encrypted communication using HTTPS
- Gained practical experience with Wireshark

---

## Interview Questions – Quick Answers

**What is TCP handshake?**  
A three-step process (SYN, SYN-ACK, ACK) used to establish a TCP connection.

**Difference between TCP and UDP?**  
TCP is reliable and connection-oriented, while UDP is faster but unreliable.

**What is DNS?**  
DNS converts domain names into IP addresses.

**What is packet sniffing?**  
Packet sniffing is capturing and analyzing network packets using tools like Wireshark.

**Why is HTTPS more secure than HTTP?**  
HTTPS encrypts data using TLS, protecting sensitive information.

---

## Deliverables

- Packet capture files (`.pcapng`)
- Wireshark analysis screenshots
- Source code (Flask login application)
- Analysis report

---

## Conclusion

This task demonstrated how insecure communication can expose sensitive data and highlighted the importance of HTTPS and encryption in cyber security. It provided hands-on experience in analyzing network traffic and understanding secure communication principles.

---

### Status: Task Completed Successfully



























