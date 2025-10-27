# Experiment - 1  
# Create a Forensic Image of a Storage Device using FTK Imager  

---

## Aim  
To create a forensically sound bit-stream image of a storage device (e.g., USB drive, hard disk) using **FTK Imager**, ensuring data integrity through hash verification.  

---

## Description  
Disk imaging is the process of creating an exact, sector-by-sector copy of a storage device. This copy, known as a **forensic image**, is crucial in digital forensics as it preserves the original evidence in an unaltered state. Investigators can then perform analysis on the image without modifying the source evidence.  

**FTK Imager** is a powerful and widely used forensic tool developed by **AccessData**. It provides a user-friendly interface for creating forensic images, verifying their integrity using hash algorithms such as **MD5** and **SHA-1**, and performing preliminary evidence analysis.  

In this experiment, we create a forensic image of a USB drive using FTK Imager, calculate and verify its hash values, and generate a detailed acquisition log to prove evidence integrity.  

---

## Tools & Equipment Used  
- FTK Imager (Software)  
- Source Drive: A USB flash drive or hard disk containing data  
- Destination Drive: An external or internal hard drive with sufficient free space to store the forensic image  

---

## Link to Download FTK Imager  
[Click to download](https://d1kpmuwb7gvu1i.cloudfront.net/Imgr/4.7.3.81%20Release/Exterro_FTK_Imager_%28x64%29-4.7.3.81.exe)

---

## Procedure  

**Step 1: Launch FTK Imager**  
   - Open **FTK Imager** on your system.  
   - Ensure you run it with **administrative privileges** so that the tool can access connected devices properly.  
<img width="1419" height="741" alt="image" src="https://github.com/user-attachments/assets/4676e597-6fae-48a5-acc9-94189605d736" />

---

**Step 2: Select the Source Drive**  
   - Go to **File → Create Disk Image**.  
<img width="1448" height="769" alt="image" src="https://github.com/user-attachments/assets/98f6e29d-8ee9-4bc1-983d-a99358332356" />
   - Choose the type of source. For a physical storage device, select **Physical Drive**.  
<img width="1444" height="763" alt="image" src="https://github.com/user-attachments/assets/ce8de162-3c27-4cf6-894d-3ae5364426d6" />
   - Click **Next**.  
   - A list of available drives appears. Select the target drive you wish to acquire and click **Finish**.  
<img width="1456" height="762" alt="image" src="https://github.com/user-attachments/assets/09329d96-0bfa-41e4-9dea-cb12002647ae" />

---

**Step 3: Choose the Image Destination**  
   - FTK Imager will now prompt you to specify the image save location.  
   - Click **Add**, then select the desired image type:  
     - **E01 (EnCase Evidence File format)** – commonly used in forensic investigations  
     - **RAW (dd format)** – bit-by-bit image copy  
<img width="1458" height="744" alt="image" src="https://github.com/user-attachments/assets/d924803e-3da4-4099-8444-135f81699490" />
   - Click **Next**.  

---

**Step 4: Enter Case Information (Optional but Recommended)**  
   - Provide relevant case details for documentation:  
     - Case Number  
     - Evidence Number  
     - Examiner Name  
     - Notes (e.g., “8GB USB drive seized from suspect”)  
<img width="1446" height="765" alt="image" src="https://github.com/user-attachments/assets/791fd633-7dd8-4e03-922e-cc772e1e618f" />
   - Click **Next**.  

---

**Step 5: Set Destination Path and File Name**  
   - Choose the folder where the forensic image will be stored.  
   - Provide a meaningful file name (e.g., `USB_8GB_Evidence.E01`).  
   - Adjust segment size or compression settings as needed (default is fine).  
   - Click **Finish**.  
<img width="1457" height="760" alt="image" src="https://github.com/user-attachments/assets/57f1a507-9993-4cd5-8bcd-b66a7b494038" />

---

**Step 6: Verify Image Options**  
   - FTK Imager displays a summary of your selections.  
   - Double-check that the **correct drive** and **destination path** are selected.  
   - Click **Start** to begin the imaging process.  
<img width="520" height="283" alt="image" src="https://github.com/user-attachments/assets/8171890c-a26d-4cfb-9fe3-41247c6e9bd3" />

---

**Step 7: Imaging and Hash Verification**  
   - FTK Imager creates a **bit-by-bit forensic image** of the source drive.  
   - Once completed, it automatically computes **MD5** and **SHA1** hash values for both the **source** and **image file**.  
   - Verify that both hash values **match**, confirming the image integrity.  

---

**Step 8: Save the Log File**  
   - FTK Imager generates a detailed log file containing:  
     - Case information  
     - Device details  
     - Hash values  
     - Start and end times  
   - Save this log file with the forensic image—it serves as proof of authenticity and evidence chain documentation.  
<img width="1053" height="250" alt="image" src="https://github.com/user-attachments/assets/b8997b9e-e4c6-44b3-ab42-6daca8f9f7ba" />



## Result  
A **forensic image** of the selected storage device was successfully created using **FTK Imager**, with verified matching hash values and complete log documentation, ensuring the integrity of the digital evidence.  

---

## Conclusion  
The experiment successfully demonstrated the creation of a forensic image using FTK Imager. Hash verification confirmed the image’s authenticity, and log files documented the acquisition process. This ensures a **forensically sound copy** that can be safely used for further analysis without altering the original evidence.  

---

## Precautions  
- Always use a **write-blocker** when acquiring evidence from suspect drives.  
- Save the image on a **different physical drive** than the source.  
- Ensure hash values (MD5, SHA1) **match exactly** to confirm image integrity.  
- Keep both the image and log files safely stored for legal and forensic documentation.  

---

## References  
- [AccessData FTK Imager User Guide](https://ad-pdf.s3.amazonaws.com/FTKImager_4_7_3_UserGuide.pdf)  
- [Kali Linux Forensics Tools](https://www.kali.org/tools/)  
- Nelson, Phillips & Steuart — *Guide to Computer Forensics and Investigations*, Cengage Learning  

---
