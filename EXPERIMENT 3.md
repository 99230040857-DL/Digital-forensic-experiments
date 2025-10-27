# Experiment - 3  
# Network Traffic Capture and Analysis using Wireshark  

---

## Aim  
To observe and analyze real-time network traffic using **Wireshark**, an open-source network packet analyzer tool, and identify packet-level communication for forensic and cybersecurity purposes.  

---

## Description  
In digital forensics and cybersecurity investigations, examining network activity helps trace malicious connections, identify unauthorized data transfers, and understand how systems communicate.  
**Wireshark** provides visibility into live network packets and supports detailed inspection of network protocols and communication behavior.  

This experiment focuses on capturing traffic, applying filters, examining packet headers, and saving results for deeper forensic analysis.  

---

## Tools and Resources  
- **Software:** Wireshark (Any version 3.x or 4.x)  
- **Operating System:** Windows / Linux  
- **File Format:** `.pcapng` (Packet Capture Next Generation)  

---

## Download Link  
[Click here to download Wireshark](https://www.wireshark.org/download.html)  

---

## Procedure  

### **Step 1: Launch Wireshark**
- Open **Wireshark** with administrator privileges to access network interfaces.  
- Wait for the home window to display available interfaces.  
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b8bff239-aa7f-4d13-a1c3-dc0b4146b9d0" />

---

### **Step 2: Choose a Network Interface**
- Identify the active interface (e.g., `Wi-Fi`, `Ethernet`, or `Local Loopback`).  
- Double-click on the interface to start capturing packets.  
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/27b666f3-c864-4799-889c-f38bb9866e7a" />

---

### **Step 3: Start Capturing Packets**
- Wireshark begins recording all incoming and outgoing packets in real-time.  
- Each row in the capture window shows:
  - **Timestamp**
  - **Source and Destination IP**
  - **Protocol**
  - **Additional Information**
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b5e9bd36-56bd-45ef-a1fb-c40b7ba2e2e5" />

---

### **Step 4: Apply Capture or Display Filters**
Filters allow analysts to focus on specific traffic types or sessions.  
Some commonly used filters are:

| Filter | Description |
|--------|--------------|
| `http` | Displays only HTTP traffic |
| `tcp.port == 80` | Displays TCP traffic on port 80 |
| `ip.addr == 10.2.24.13` | Shows packets related to a specific IP address |

**Example:**
- Filtering HTTP traffic → `http`  
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/4ea93221-22a6-4561-b851-34cb201db1d6" />

- Filtering TCP port 80 packets → `tcp.port == 80`  
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6c28463e-db19-44ee-8f3a-bca8b2716435" />

---

### **Step 5: Inspect Individual Packets**
- Click on any packet to expand and view its internal structure.  
- The hierarchical breakdown includes:
  - **Frame Layer:** General metadata and packet number  
  - **Ethernet Layer:** Source and destination MAC addresses  
  - **IP Layer:** Source and destination IP addresses  
  - **Transport Layer (TCP/UDP):** Port numbers and flags  
  - **Application Layer:** Protocol-specific data (HTTP, DNS, etc.)  
- The lower pane displays the raw hexadecimal and ASCII data of the packet.  
<img width="1603" height="880" alt="image" src="https://github.com/user-attachments/assets/9f09f191-0128-4758-a26c-f794dae30365" />

---

### **Step 6: Save Captured Data**
- Once enough traffic has been recorded, go to:  
  **File → Save As → Choose Location and File Name**
- Save the file with `.pcapng` extension for later review or forensic reporting.  
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/804d5ea5-7c6c-40b9-8a6a-dddc356532f8" />

---

### **Step 7: Analyze Captured Packets**
- Use **Statistics → Protocol Hierarchy** to view a summary of network protocols.  
- Check for abnormal patterns like:
  - Unusual IP addresses  
  - Repeated failed handshakes  
  - Suspicious or unexpected protocols  

---

## Result  
Wireshark successfully captured and analyzed live network traffic. The experiment demonstrated the use of capture filters, detailed packet inspection, and the process of saving and examining packet data for forensic investigation.  

---

## Inference  
This experiment provided hands-on experience in packet-level traffic analysis, which is fundamental for detecting network threats, intrusion attempts, and verifying secure communications.  

---

## References  
- [Wireshark Official Website](https://www.wireshark.org)  
- [Wireshark User Documentation](https://www.wireshark.org/docs/)  
- [Cybersecurity Forensics Guide - Kali Linux Docs](https://www.kali.org/docs/)  
