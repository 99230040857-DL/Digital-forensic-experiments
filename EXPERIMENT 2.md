# Experiment - 2  
# Recover Deleted or Damaged Files from a Storage Device using TestDisk  

## Aim  
To recover deleted or damaged files from a storage device using **TestDisk**, a forensic recovery tool.  

---

## Description  
In digital forensics, recovering deleted or corrupted files is an essential step during investigations. When files are deleted, their entries are removed from the file system, but the actual data often remains on the storage media until overwritten. **TestDisk** is an open-source forensic tool designed to recover lost partitions, fix disk errors, and restore deleted files.  

This experiment demonstrates how to use **TestDisk** in **Kali Linux** to identify and restore deleted or damaged files from a storage device, ensuring data integrity for forensic analysis.  

---

## Tools & Equipment Used  
- TestDisk (Software)  
- Source Drive: A USB flash drive or hard disk containing data  
- Destination Drive: Internal hard drive with sufficient free space to store the recovered data  

---

## Link to Download TestDisk  
[Click to download](https://www.cgsecurity.org/Download_and_donate.php/testdisk-7.3-WIP.win64.zip)

---

## Procedure  

**Step 1: Launch TestDisk**  
   - Open the TestDisk tool from the terminal using the following command:  
     ```bash
     sudo testdisk
     ```  
   - Run it with administrative privileges for full access.  
<img width="1118" height="667" alt="image" src="https://github.com/user-attachments/assets/65cc35f0-de1e-4e04-bdd7-de61a9ea6933" />

---

**Step 2: Create or Append Log File**  
   - When TestDisk opens, it asks to create a log file.  
   - Choose **Create** to generate a new log for this recovery session.  
<img width="1125" height="676" alt="image" src="https://github.com/user-attachments/assets/3c806e89-f919-4390-99ec-ca8f1b3af6bf" />

---

**Step 3: Select the Storage Device**  
   - TestDisk lists all available storage devices connected to the system.  
   - Use the **arrow keys** to select the target device where the files were deleted.  
   - Press **Enter** to proceed.  
<img width="1125" height="676" alt="image" src="https://github.com/user-attachments/assets/c856dcc4-b23e-49e9-9ebb-cb31b94a4ef1" />

---

**Step 4: Select Partition Table Type**  
   - TestDisk automatically detects the partition table type (e.g., Intel/MBR, EFI GPT).  
   - Confirm the suggested type by pressing **Enter**.  
<img width="1128" height="658" alt="image" src="https://github.com/user-attachments/assets/e4f2d9f8-3745-42c7-81b4-b4ac6a5cb3bf" />

---

**Step 5: Analyze the Disk**  
   - Select **Analyse** and then choose **Quick Search** to find lost partitions.  
   - If not found, use **Deeper Search** for a more thorough scan.  
<img width="1129" height="671" alt="image" src="https://github.com/user-attachments/assets/e65e5c4a-00ac-4a81-9f25-685f902aaf6e" />

---

**Step 6: Access Advanced Options**  
   - Go to **Advanced → File System Utilities**.  
   - Select the partition where files were deleted.  
   - Press **Enter** to view the file list.  
<img width="1119" height="671" alt="image" src="https://github.com/user-attachments/assets/8fb1f28c-5a6f-467a-bd94-9f762e4d98e8" />

---

**Step 7: View Deleted Files**  
   - Deleted files appear in **red** in the file list.  
   - Use arrow keys to navigate to the deleted files you want to recover.  
<img width="1125" height="684" alt="image" src="https://github.com/user-attachments/assets/2f17e44c-855f-48ea-ae24-47da636e00c2" />

---

**Step 8: Recover Deleted Files**  
   - Highlight the deleted files and press **C** (uppercase) to copy.  
   - Choose a **different drive or folder** as the destination (for example, Desktop or another partition).  
<img width="1137" height="673" alt="image" src="https://github.com/user-attachments/assets/9c75d413-8122-4aed-9c59-a7105194a93a" />

---

**Step 9: Verify Recovered Files**  
   - After recovery, open the destination folder to check whether the files have been successfully restored.  
   - You can use the following command in Kali Linux:  
     ```bash
     cd ~/Desktop
     ls
     ```  
   - Ensure the recovered files are intact and functional.  

---

## Result  
Deleted or damaged files were successfully recovered from the storage device using **TestDisk** in Kali Linux. The recovered files retained their integrity and were suitable for forensic analysis.  

---

## Conclusion  
This experiment demonstrated how to use **TestDisk** to recover deleted or lost files from a storage device. The tool effectively scans partitions, identifies deleted data, and restores it without altering the source media. This ensures data integrity, which is critical for digital forensic investigations.  

---

## Precautions  
- Always recover files to a **different drive** to avoid overwriting data.  
- Avoid using the affected drive before completing recovery.  
- Run TestDisk with **root privileges** for complete disk access.  
- Keep a backup of the TestDisk log file for documentation.  

---

## References  
- [TestDisk Official Website](https://www.cgsecurity.org/wiki/TestDisk)  
- [Kali Linux Tools Documentation](https://www.kali.org/tools/testdisk/)  
- Digital Forensics Using Open-Source Tools – Elsevier Publications  

---
