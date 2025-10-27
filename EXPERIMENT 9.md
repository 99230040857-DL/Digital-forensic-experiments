# Experiment 9
# Use Process Explorer to Identify Suspicious Processes

---
## Aim
To demonstrate the use of Process Explorer in identifying, analyzing, and investigating suspicious processes running on a Windows system for digital forensics purposes.

---
## Description
Process Explorer is an advanced system monitoring tool that provides detailed information about which handles and DLLs processes have opened or loaded. This experiment focuses on using Process Explorer to identify potentially malicious processes, analyze their behavior, and determine their impact on system security.

---
## Tools Used
1. Process Explorer (Sysinternals Suite)
2. Windows Operating System
3. Test processes (both legitimate and suspicious)
4. VirusTotal integration (for malware verification)

---
## Prerequisites
1. Download and install Process Explorer from Microsoft Sysinternals
2. Administrative privileges on the Windows system
3. Internet connection (for VirusTotal integration)
4. Basic understanding of Windows processes

---
## Procedure

### 1. Installation and Setup
1. Download Process Explorer from Microsoft's website
2. Extract and run ProcessExplorer.exe
3. Configure Process Explorer settings:
   - Enable "Verify Image Signatures"
   - Configure VirusTotal integration
   
<img width="1008" height="777" alt="image" src="https://github.com/user-attachments/assets/ce965858-569c-41b9-929a-1d453f2bce1e" />



<img width="1002" height="759" alt="image" src="https://github.com/user-attachments/assets/91e85eb9-2e3e-4bf5-bf66-f9fe0fd67ce2" />


### 2. Basic Process Analysis
1. Observe the two-pane display:
   - Upper pane: Process list
   - Lower pane: Handle or DLL view

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ec0dcd31-1bb2-4c66-8098-acd0f9fdbf8a" />


2. Understanding the color coding:
   - Purple: Packed processes
   - Pink: Services
   - Blue: New processes
   - Red: Terminated processes
<img width="1240" height="1080" alt="image" src="https://github.com/user-attachments/assets/9f4d849e-e4bd-4bc5-944f-904b203e5db0" />


### 3. Identifying Suspicious Processes
1. Check for unusual process names or locations
2. Look for processes with:
   - No description
   - No company name
   - Suspicious file locations
   - High CPU or memory usage

### 4. Process Properties Analysis
1. Right-click suspicious process → Properties
2. Examine:
   - Image path
   - Command line
   - Parent process
   - Start time
   - User account
   
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/76b7b451-cbe7-493b-b6e5-595a1941f98f" />


### 5. VirusTotal Integration
1. Enable VirusTotal submission
2. Check suspicious files:
   - Right-click process
   - Select "Check VirusTotal"
   
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c166eacd-7ac5-4100-a98a-3ea693565226" />

### 6. DLL and Handle Investigation
1. View loaded DLLs:
   - Select process
   - Lower pane: DLL view
   
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/2bdb240c-9069-4e38-b331-8b3b1bb9dd58" />

2. Analyze handles:
   - Switch to handle view
   - Look for suspicious file/registry handles
   
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f27e85c7-41c3-448b-a531-31a47f904dfc" />


### 7. Tree View Analysis
1. View process relationships:
   - Enable tree view
   - Identify parent-child relationships
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/2c21494e-c0da-4ff7-80c3-cc0bc597ac49" />

---
## Results
The experiment successfully demonstrated:

1. Process Identification:
   - Total processes analyzed: [X]
   - Suspicious processes identified: [X]
   - Confirmed malicious processes: [X]

2. System Analysis:
   - CPU usage patterns
   - Memory usage patterns
   - Network connection analysis
   - File handle investigation

3. Key Findings:
   - Types of suspicious activities detected
   - Common characteristics of malicious processes
   - System resource impact

---
## Conclusion
Process Explorer is an effective digital forensics tool for identifying and analyzing suspicious processes on Windows systems. 

Key benefits:
1. Real-time monitoring of all running processes
2. Quick identification of unsigned or suspicious executables
3. Easy verification of processes using VirusTotal
4. Detailed view of process relationships and loaded DLLs

The tool is recommended for initial system investigation and ongoing security monitoring of Windows environments.

---
