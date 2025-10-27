# Experiment – 4  
## Email Header Analysis and Spoof Detection using Mail Header Analyzer (MHA)

---

## Aim
To analyze the structure and contents of email headers using the Mail Header Analyzer (MHA) tool in order to trace the true origin of an email and detect any signs of spoofing.

---

## Description
Email spoofing is a cyber technique used by threat actors to forge the sender’s address in an attempt to trick recipients into believing a message is legitimate.  
By carefully examining email headers, forensic analysts can verify sender authenticity, track the relay path of the email, and assess the integrity of authentication mechanisms such as **SPF**, **DKIM**, and **DMARC**.

The **Mail Header Analyzer (MHA)** is an open-source, web-based utility that decodes complex email headers. It presents detailed insights on:
- Message routing and delays  
- Originating IP address  
- Authentication results  
- Potential indicators of spoofing  

---

## Tools & Resources
- **Mail Header Analyzer (MHA)**  
- **Email Header** (from a test or suspicious message)

**Access Tool:** [Mail Header Analyzer](https://mha.azurewebsites.net/)

---

## Procedure

### 1. Obtain the Raw Email Header
- Open the suspicious or test email in your client (e.g., Gmail, Outlook).  
- Locate and open the full email header or “View Original Message” option.  
- Copy the entire raw header text.  

<img width="1907" height="1015" alt="image" src="https://github.com/user-attachments/assets/f084ef56-926e-4634-9e84-debaa61d974e" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/7dc65de6-ea25-4645-9b87-250bfb61df97" />

---

### 2. Access the Mail Header Analyzer (MHA)
- Visit **[https://mha.azurewebsites.net/](https://mha.azurewebsites.net/)** in your browser.  
- Paste the copied email header into the input section.  

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/836100b6-85f8-4c2f-9466-17747960a9e2" />

---<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ac6ba007-605f-4493-98be-a90c62fbd6ce" />


### 3. Analyze the Header
- Click on **Analyze** to begin processing the email header.  
- MHA will display detailed information including:
  - **Source IP address** of the sender  
  - **Mail relay servers** involved in the message path  
  - **Authentication results** (SPF, DKIM, DMARC)  

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0adc54b8-545f-4c09-9960-6e6505f76222" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/261a8cb3-9274-492f-8f2e-9172fb56cba6" />

---

### 4. Examine Authentication Checks
- Verify **SPF**, **DKIM**, and **DMARC** results.  
- Any failed or missing authentication check can indicate a spoofed or unverified sender.  

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8f4a934e-5590-44eb-8aab-c4817a759693" />

---

### 5. Inspect the Mail Path
- Review the full route the message traveled through.  
- Compare the **originating IP** and **sending domain** with the claimed sender address.  
- Note any unusual relay servers or delay timestamps.  

<img width="1914" height="434" alt="image" src="https://github.com/user-attachments/assets/1b457a49-b6cd-4cc9-a9f3-e808a9fdab79" />

---

### 6. Identify Spoofing Indicators
- Look for inconsistencies such as:  
  - Mismatched sender domain and originating IP  
  - Failed SPF/DKIM/DMARC validations  
  - Relays that do not belong to the sender’s organization  
  - Abnormal delays between hops  

**Example of a suspicious email header with abnormal delay:**  
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b014467a-34a1-4b03-b332-f9a8e8d11839" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f7750d71-834f-4139-b2bd-699c804bbfe9" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d3f8411e-59a5-4fef-82fa-0564140367de" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/dd99c34c-7078-4f4d-bb6b-4de366c99337" />

---

## Result
The email header was successfully analyzed using the Mail Header Analyzer.  
Key findings included mismatched sender information and failed authentication checks, confirming potential signs of spoofing.  
This process demonstrates how forensic analysis of email headers can help detect and prevent fraudulent or malicious email activity.

---

## Conclusion
Through this experiment, the process of identifying spoofed or forged emails was successfully demonstrated using MHA.  
By examining authentication records, IP paths, and server hops, investigators can reliably trace email origins and enhance cybersecurity awareness.

---

## References
- [Mail Header Analyzer (MHA) Tool](https://mha.azurewebsites.net/)
- RFC 5322: Internet Message Format
- RFC 7208: Sender Policy Framework (SPF)
- RFC 6376: DomainKeys Identified Mail (DKIM)

---
