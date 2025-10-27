# Experiment 10
# Use Ghidra to Disassemble and Analyze Malware Code

---
## Aim
To demonstrate the process of using Ghidra to disassemble, decompile, and analyze malware code for understanding its functionality and potential threats.

---
## Description
Ghidra is a powerful software reverse engineering (SRE) framework developed by NSA. This experiment focuses on using Ghidra's features to analyze malware samples, understand their behavior, identify malicious functions, and document findings. The analysis will help in understanding the malware's capabilities and potential impact on systems.

---
## Tools Used
1. Ghidra (latest version)
2. Java Development Kit (JDK)
3. Virtualized environment (for safety)
4. Sample malware (in a controlled environment)
5. Windows/Linux operating system

---
## Prerequisites
1. Isolated analysis environment (Virtual Machine)
2. Java Development Kit installed
3. Ghidra installed and configured
4. Test malware samples (safely contained)
5. Basic understanding of assembly language

---
## Procedure

### 1. Environment Setup
1. Install Java Development Kit
2. Download and install Ghidra
3. Configure isolated analysis environment
4. Verify Ghidra launches successfully

<img width="1077" height="493" alt="image" src="https://github.com/user-attachments/assets/a0e7382f-50cc-4cb7-94cb-2a529f5358ec" />

### 2. Project Creation
1. Create new project:
   - File → New Project
   - Select Non-Shared Project
   - Choose project location
   

<img width="911" height="628" alt="image" src="https://github.com/user-attachments/assets/a0163594-4b74-4a80-a69a-1542aaa91478" />



<img width="911" height="628" alt="image" src="https://github.com/user-attachments/assets/1b531f76-7ca7-4ba5-96d6-a3f0f8839798" />


2. Import malware sample:
   - File → Import File
   - Select malware sample
   - Configure import options

   <img width="911" height="628" alt="image" src="https://github.com/user-attachments/assets/7c59d833-7ba5-4368-9b40-40b88c9ea9fa" />



<img width="911" height="628" alt="image" src="https://github.com/user-attachments/assets/17c964d8-130c-45cc-8a2f-0abce6e13abd" />


### 3. Initial Analysis
1. Double-click imported file to analyze
2. Wait for auto-analysis to complete
3. Review initial analysis results:
   - Functions identified
   - Strings detected
   - Entry points located
   
<!-- [Insert Screenshot: Place screenshot of auto-analysis results] -->

<img width="817" height="893" alt="image" src="https://github.com/user-attachments/assets/c308f6ea-5867-4771-8fea-aca1c7d93934" />

![Fig-1](Output%20Screenshot/Exp10/Screenshot%20From%202025-10-26%2001-30-50.png)

### 4. Code Analysis
1. Navigate through Program Trees:
   - Functions
   - Labels
   - Data Types
   
<!-- [Insert Screenshot: Place screenshot of program structure] -->

<img width="1651" height="747" alt="image" src="https://github.com/user-attachments/assets/31755fec-7407-44fd-bc64-b1add58bdcd0" />

2. Examine Decompiled Code:
   - Use Decompiler window
   - Analyze function logic
   - Identify suspicious operations
   
<!-- [Insert Screenshot: Place screenshot of decompiled code view] -->

<img width="659" height="696" alt="image" src="https://github.com/user-attachments/assets/32c16d36-c357-45ea-a8c6-a496cb41398e" />

### 5. Function Analysis
1. Identify main functions:
   - Entry points
   - Important API calls
   - String references
   
<!-- [Insert Screenshot: Place screenshot showing important functions] -->

<img width="1667" height="694" alt="image" src="https://github.com/user-attachments/assets/c203830d-f735-42b7-8ac0-8bd8324f3ecb" />

2. Analyze suspicious functions:
   - Network operations
   - File system operations
   - Registry modifications
   
<!-- [Insert Screenshot: Place screenshot of suspicious function analysis] -->

<img width="1667" height="694" alt="image" src="https://github.com/user-attachments/assets/b62c3a07-edba-4cbe-ad4f-be952c6d27b6" />

### 6. String Analysis
1. Examine string references:
   - URLs
   - File paths
   - Registry keys
   - Command strings
   
<!-- [Insert Screenshot: Place screenshot of string analysis] -->

<img width="1667" height="694" alt="image" src="https://github.com/user-attachments/assets/7d70530c-5776-475e-a30a-d87f366e296f" />

### 7. Cross-Reference Analysis
1. Track function calls:
   - Who calls this function
   - What this function calls
   
### 8. Memory Analysis
1. Review memory layout:
   - Sections
   - Segments
   - Permissions
   
<!-- [Insert Screenshot: Place screenshot of memory layout] -->

<img width="1667" height="694" alt="image" src="https://github.com/user-attachments/assets/363d8edd-a63a-40ce-a065-26b9b3b5a861" />

---
## Results
The experiment successfully demonstrated:

1. Code Analysis Results:
   - Total functions analyzed:[✅]
   - Suspicious functions identified: [X]
   - Malicious behaviors detected: [X]

2. Malware Capabilities Identified:
   - Network communication methods
   - File system interactions
   - System modifications
   - Persistence mechanisms

3. Key Findings:
   - Primary malware functionality
   - Evasion techniques used
   - System impact assessment
   - Network indicators

---
## Conclusion
Ghidra proved to be a powerful tool for malware analysis and reverse engineering.

Key achievements:
1. Successfully disassembled and decompiled malware code
2. Identified malicious functions and system interactions
3. Extracted indicators of compromise for detection
4. Understood malware behavior and persistence mechanisms

**Important**: Always perform malware analysis in isolated virtual environments to prevent system compromise.

The tool is highly recommended for digital forensics professionals conducting malware investigation and threat analysis.

Best Practices Identified:
1. Systematic analysis approach
2. Documentation of findings
3. Safe handling procedures
4. Indicator extraction

[Note: Please add actual screenshots of your experiment execution in the designated places marked with "Insert Screenshot" tags. Also, replace all placeholder values in square brackets with actual experimental data. Remember to handle malware samples in a safe, isolated environment only.]

---
## Safety Warning
⚠️ **IMPORTANT**: Always analyze malware in an isolated environment. Never execute suspicious code on production systems. Use appropriate safety measures including:
- Isolated virtual machines
- Network isolation
- Proper handling procedures
- Data backup
- Safety protocols

---
