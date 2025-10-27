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
   - _[Insert screenshot: `images/autopsy_welcome.png` ]_

2. **Create New Case**
   - Click *Create New Case*.
   - Example details:
     - Case name: `Exp5_Autopsy_Practice_<YourInitials>`
     - Examiner: `<Your Name>`
     - Case number: `EXP5-2025-<ID>`
   - _[Insert screenshot: `images/new_case.png` ]_

3. **Configure Case Database**
   - Select *Single-user database* (for practice).
   - Confirm DB location inside the case folder.
   - _[Insert screenshot: `images/db_config.png` ]_

4. **Add Data Source**
   - Add → *Disk Image or VM file* → browse to `evidence01.E01`.
   - Verify the image hash matches the saved hash file.
   - _[Insert screenshot: `images/add_data_source.png` ]_

5. **Configure Ingest Modules**
   - Select modules:
     - File Type Identification
     - Keyword Search
     - Recent Activity
     - EXIF Parser
     - Hash Lookup
   - Save ingest profile for reproducibility.
   - _[Insert screenshot: `images/ingest_modules.png` ]_

6. **Start Ingest / Analysis**
   - Click *Finish* to start ingest.
   - Monitor the ingest progress pane and record start/end times.
   - _[Insert screenshot: `images/ingest_progress.png` ]_

7. **Initial Observations & Export**
   - Check *File Types* and *Keyword Hits* for quick findings.
   - Export an ingest summary (HTML/CSV) for reporting.
   - _[Insert screenshot: `images/results_overview.png` ]_

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

