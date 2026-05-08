# Wireshark Lab - HTTP Traffic Analysis

## 🎯 Objective
Educational lab using Wireshark to analyze HTTP traffic and demonstrate how credentials can appear in plain text, highlighting the importance of secure protocols.


## 🛠️ Tools Used
- **Wireshark** - Network protocol analyzer
- **Firefox** - Web client to generate HTTP traffic
- **Ubuntu Linux** - Analysis environment

## 📷 Evidence
![HTTP Traffic Example](/http_plaintext_credentials_leaked.png)

The screenshot illustrates how an HTTP `POST` request can expose data in plain text when transmitted without encryption.
- **Username:** `admin1000`
- **Phone:** `123456`

This example highlights the risks of using unencrypted protocols, showing how sensitive information can be visible to anyone monitoring the network.

## 🔍 Technical Analysis
1. **Vulnerable Protocol:** HTTP/1.1 sends data unencrypted at Layer 7
2. **Capture Method:** Filter `http.request.method == POST` + `Follow HTTP Stream`
3. **Risk:** Exposure of PII and credentials on public WiFi, corporate networks, on compromised infrastructure

## 🛡️ Blue Team Mitigation
1. **Enforce HTTPS** with valid TLS 1.3 certificates
2. **Implement HSTS** headers to prevent protocol downgrade attacks
3. **Disable port 80** on production web servers
4. **User Awareness:** Educate users about risks of public WiFi networks

## 📚 Demonstrated Skills
- Network traffic analysis with Wireshark
- Identification of insecure protocols
- Digital forensics evidence documentation
- Technical security report writing 
- Understanding of MITM attack vectors

---
**Disclaimer:** Lab conducted in a controlled environment for educational and professional portfolio purposes only.
