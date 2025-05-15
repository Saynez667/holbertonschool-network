# 🌐 What Happens When You Type https://www.google.com?

**A Deep Dive into Web Infrastructure & Networking**  
*Technical breakdown of browser-to-server communication flow*

---

## 📝 Blog Post: [Full Explanation on Medium](https://medium.com/@yourusername/web-infrastructure-deep-dive-123456)

### Key Stages Explained:

1. **DNS Resolution**  
   - Browser checks local cache → OS cache → ISP resolver  
   - Recursive query to root → .com TLD → Google's nameservers [9][11]

2. **TCP/IP Handshake**  
   - 3-way handshake (SYN, SYN-ACK, ACK) establishes connection  
   - Ensures reliable data transmission [8][11]

3. **Firewall Inspection**  
   - Checks packet headers against security rules  
   - Allows HTTPS (port 443) traffic [2][8]

4. **HTTPS/SSL Encryption**  
   - TLS handshake: certificate validation & key exchange  
   - Encrypts traffic with AES-256 [2][11]

5. **Load Balancer Routing**  
   - Distributes requests using round-robin algorithm  
   - Active-active configuration for high availability [2][6]

6. **Web Server Processing**  
   - Nginx serves static assets (HTML/CSS/JS)  
   - Handles 50k+ concurrent connections [3][8]

7. **Application Server Logic**  
   - Node.js/Python processes dynamic content  
   - Generates personalized search results [3][11]

8. **Database Interaction**  
   - MySQL cluster handles read/write operations  
   - Primary-replica replication for data consistency [3][9]

---

## 🔄 System Flow Diagram  
![Infrastructure Diagram](https://i.imgur.com/your-diagram-image.png)  
*Created with [draw.io](https://app.diagrams.net/)*

### Diagram Components:
1. DNS resolution chain
2. Encrypted HTTPS tunnel
3. Firewall filtering
4. HAProxy load balancer
5. Web/application server tier
6. Database cluster with replication

---

## 📚 Key Technical Concepts
| Term          | Explanation                          | Relevance |
|---------------|--------------------------------------|-----------|
| **SPOF**      | Single point of failure              | Avoid in load-balanced setups |
| **QPS**       | Queries per second metric            | Capacity planning |
| **TLS 1.3**   | Latest encryption protocol            | Security compliance |
| **ACID**      | Database transaction properties       | Data integrity |

---

## 📂 Project Structure
```sh
what_happens_when_your_type_google_com_in_your_browser_and_press_enter/
├── 0-blog_post # Medium article link
└── 1-what_happen_when_diagram # draw.io diagram URL
```
---

## 🔍 Resources
1. [DNS Explained](https://www.cloudflare.com/learning/dns/)
2. [HTTPS Encryption Guide](https://https.cio.gov/)
3. [Load Balancing Strategies](https://www.nginx.com/resources/glossary/load-balancing/)

---

**👨💻 Author**  