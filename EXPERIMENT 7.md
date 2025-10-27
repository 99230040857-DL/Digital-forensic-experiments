# Experiment 7 
# Android Device Forensic Acquisition using ADB Logical Backup

---
## Aim
To perform logical acquisition of data from an Android device using Android Debug Bridge (ADB) backup functionality.

---

## Description
This experiment demonstrates the forensic acquisition of data from an Android device using ADB's built-in backup functionality. The process includes creating a logical backup, verifying its integrity through hashing, and analyzing the extracted contents while maintaining forensic principles.

---
## Tools Used
1. Android Debug Bridge (ADB)
2. Android Device
3. USB Cable
4. Android Backup Extractor (abe.jar)
      .Download Android Backup Extractor from GitHub:
   ```bash
   git clone https://github.com/nelenkov/android-backup-extractor/releases/tag/latest
   ```
5. SHA256 hashing tool

---
## Prerequisites
1. Android device with:
   - USB debugging enabled
   - At least 50% battery life
   - Device unlocked and screen active
2. Computer with:
   - ADB installed and configured
   - Java Runtime Environment (JRE)
   - Required USB drivers installed

---
## Procedure

### 1. Device Connection and Verification
1. Connect Android device via USB
2. Verify connection using ADB:
```powershell
   adb devices

```<img width="605" height="120" alt="image" src="https://github.com/user-attachments/assets/1382a24c-7fc3-4116-a9f1-a0311dcf2fd1" />

<!-- [Insert Screenshot: ADB devices list output] -->

3. Check device details:
```powershell
   adb shell getprop ro.product.model
   adb shell getprop ro.build.version.release

```<img width="939" height="150" alt="image" src="https://github.com/user-attachments/assets/f0a6b8bb-60f5-49d3-9262-c76928a7e652" />

<!-- [Insert Screenshot: Device properties output] -->

### 2. Creating Full ADB Logical Backup
1. Create full backup including shared storage:
```powershell
   adb backup -f device_backup.ab -all -system -shared -apk
```

<img width="944" height="146" alt="image" src="https://github.com/user-attachments/assets/4ef228a5-b440-45a1-93f0-8fca46ab820b" />
<!-- [Insert Screenshot: Backup creation dialog on device] -->

2. Monitor backup progress:
```powershell
   dir device_backup.ab
```

<img width="913" height="115" alt="image" src="https://github.com/user-attachments/assets/7c4621be-7486-49dd-8b9b-d2a5fbbee93b" />
<!-- [Insert Screenshot: File size and creation time] -->

### 3. Backup Integrity Verification
1. Generate SHA256 hash of backup file:
```powershell
   certutil -hashfile device_backup.ab SHA256
```
<!-- [Insert Screenshot: Hash output] -->

<img width="913" height="115" alt="image" src="https://github.com/user-attachments/assets/d32c3e13-dc35-40c6-93f1-223b2036d993" />

### 4. Creating External Storage Only Backup
1. Verify connection using ADB:
```powershell
   adb devices
```

<img width="1153" height="267" alt="image" src="https://github.com/user-attachments/assets/19d5d2a7-39e1-4823-afbd-7acea74a0e14" />
<!-- [Insert Screenshot: Shared storage backup dialog] -->

2. Find the external storage path:
```powershell
   adb shell ls /storage
```
   You'll see something like:
emulated  self  XXXX-XXXX
The one with numbers (e.g. XXXX-XXXX) is your SD card.


<img width="1153" height="178" alt="image" src="https://github.com/user-attachments/assets/4ac9d2b3-65b3-48ad-a845-ac6d66347462" />

3. Create a backup folder on the host computer, for example:
```poweshell
   mkdir D:\android_backup
```

4. Back up only the SD card folder:
Replace XXXX-XXXX with your card ID:
```powershell
   adb pull /storage/XXXX-XXXX D:\phone_backup\
```
🔹 This copies only SD card contents to your laptop (folder D:\android_backup\).
🔹 It won’t touch internal storage or system data.

5. Verify backup creation:

<!-- [Insert Screenshot: Shared storage backup file details] -->

<img width="1172" height="461" alt="image" src="https://github.com/user-attachments/assets/591cc17f-5b3a-41b9-adbc-64db45a83204" />

<img width="1452" height="671" alt="image" src="https://github.com/user-attachments/assets/aaeafd12-59a6-4672-a107-8db2a3739b0b" />

6. Compare sizes of full backup vs shared storage backup:
<!-- [Insert Screenshot: Size comparison of backup files] -->

<img width="1205" height="121" alt="image" src="https://github.com/user-attachments/assets/1e1ad66e-51f7-4dd2-b0c2-a90c1c785f89" />


### 5. Converting Backup to TAR Format
1. Download Android Backup Extractor (abe.jar)
2. Convert .ab file to .tar:
```powershell
   tar -cvf sd_backup.tar "C:\Users\K CHANDRA SEKHAR\backup"
```

<img width="1172" height="461" alt="image" src="https://github.com/user-attachments/assets/309b6669-4eda-4589-806b-9a4bcc9bcadf" />

<img width="1452" height="671" alt="image" src="https://github.com/user-attachments/assets/105847ae-9e57-48b3-b177-cb397472840e" />

<!-- [Insert Screenshot: Conversion process output] -->

### 6. Extracting Backup Contents
1. Extract TAR archive:
```powershell
   tar -xvf sd_backup.tar -C D:\extracted_backup\
```

<img width="1433" height="630" alt="image" src="https://github.com/user-attachments/assets/14d25729-4556-40c5-abd2-b58e616af128" />
<!-- [Insert Screenshot: Extraction process] -->

2. List extracted contents:
```powershell
   dir extracted_backup /s
```
<!-- [Insert Screenshot: Directory listing] -->

<img width="1212" height="834" alt="image" src="https://github.com/user-attachments/assets/755a7a53-48e2-4f02-ba1b-593bb614ecfa" />

### 7. Data Analysis

1. Common locations to examine:
   - apps/com.android.providers.contacts/d_*/databases/contacts2.db
   - apps/com.android.providers.telephony/d_*/databases/mmssms.db
   - apps/com.android.providers.media/d_*/databases/external.db

2. Analyze database contents using SQLite Browser

---
## Results
Document the following findings:
1. Backup File Details:
   - Size: [Size in MB]
   - Creation Time: [Timestamp]
   - SHA256 Hash: [Hash value]

2. Extracted Content Statistics:
   - Number of applications: [Count]
   - Total files extracted: [Count]
   - Key databases found: [List]

---

## Conclusion
The experiment successfully demonstrated the process of performing logical acquisition from an Android device using ADB backup. This method proves effective for basic forensic acquisition while maintaining evidence integrity through proper documentation and hash verification.

---
