# Experiment — Autopsy Case Creation & Evidence Import (Experiment 5)

---

## Aim
To create a new case in Autopsy, import a disk image as evidence, configure ingest modules, and begin a basic analysis while documenting each step for reproducibility and chain-of-custody.

---

## Tools Used
- Autopsy 4.21.0 (or later)
- Sample disk image (e.g., `evidence01.E01`)
- Host: Windows 10 / Linux with sufficient disk space
- Hashing utility (md5/sha256) for verifying evidence integrity

---

## Pre-checks
1. Verify image integrity: `sha256sum evidence01.E01 > evidence01.sha256`
2. Ensure Autopsy has write permissions to the case directory
3. Confirm available disk space

---

## Procedure

1. **Launch Autopsy**
   - Start Autopsy and wait for the welcome screen.
<img width="689" height="504" alt="image" src="https://github.com/user-attachments/assets/1c1f4d93-bbbe-4af6-90d5-24b369674f07" />

2. **Create New Case**
   - Click *Create New Case*.
   - Example details:
     - Case name: `Exp5_Autopsy_Practice_<YourInitials>`
     - Examiner: `<Your Name>`
     - Case number: `EXP5-2025-<ID>`

3. **Configure Case Database**
   - Select *Single-user database* (for practice).
   - Confirm DB location inside the case folder.

4. **Add Data Source**
   - Add → *Disk Image or VM file* → browse to `evidence01.E01`.
   - Verify the image hash matches the saved hash file.
<img width="1089" height="707" alt="image" src="https://github.com/user-attachments/assets/d95540b3-e42a-4001-9ca2-c461c71d6945" />

5. **Configure Ingest Modules**
   - Select modules:
     - File Type Identification
     - Keyword Search
     - Recent Activity
     - EXIF Parser
     - Hash Lookup
   - Save ingest profile for reproducibility.
<img width="1091" height="709" alt="image" src="https://github.com/user-attachments/assets/1b80a714-4b15-4457-8bca-8dca231eac3b" />

6. **Start Ingest / Analysis**
   - Click *Finish* to start ingest.
   - Monitor the ingest progress pane and record start/end times.
<img width="1100" height="694" alt="image" src="https://github.com/user-attachments/assets/6786254b-2a1d-45b7-abca-68941c63a35f" />

7. **Initial Observations & Export**
   - Check *File Types* and *Keyword Hits* for quick findings.
   - Export an ingest summary (HTML/CSV) for reporting.
<img width="1095" height="708" alt="image" src="https://github.com/user-attachments/assets/839cc71d-d575-478d-84fa-52735e56b8ad" />

---

## Evidence Handling / Chain of Custody
- Save original image file name, location, and hash.
- Keep a case log: who handled the evidence, when, and what actions were taken.
- Perform analysis on working copies; keep originals read-only.

---

## Result
- Case created and evidence imported with verified hash.
- Ingest modules ran and produced initial artifacts ready for deeper analysis.

---

## Conclusion & Next Steps
- Next: timeline building, deeper keyword sweeps, browser history and email artifact analysis.
- Maintain case log and export final reports as evidence.

---

## Appendix
- Example hash command: `sha256sum evidence01.E01 > evidence01.sha256`
- Suggested keywords for practice: `password, login, invoice, bank, transfer`
- Paths:
  - Report: `reports/experiment_report.pdf`
  - Logs: `logs/autopsy.log`

