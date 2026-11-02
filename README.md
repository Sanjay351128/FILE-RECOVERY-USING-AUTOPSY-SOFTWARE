# FILE-RECOVERY-USING-AUTOPSY-SOFTWARE

## AIM
To use **Autopsy Digital Forensics Tool** to retrieve deleted files from a disk image.

---

## REQUIREMENTS
- **Operating System**: Windows 10/11, macOS, or Linux
- **Tool**: [Autopsy Digital Forensics](https://www.autopsy.com/)  
- **Test Data**: Disk image file (`disk.dd`, `disk.img`, `.E01`)

---

## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Install Autopsy]
    B --> C[Create New Case in Autopsy]
    C --> D[Add Data Source: Disk Image]
    D --> E["Run File System & Data Recovery Modules"]
    E --> F[Locate Deleted Files in Results]
    F --> G[Recover and Export Deleted Files]
```
## DESIGN STEPS:
### Step 1:
Open Autopsy and create a new case with appropriate case details.

### Step 2:
Add a disk image as a data source and let Autopsy analyze the content.

### Step 3:
Navigate to the "Deleted Files" section in Autopsy and examine or recover the deleted files.

## PROGRAM:
### Install Autopsy
```bash
# Download Autopsy from:
# https://www.autopsy.com/
# Install following the setup wizard.
```
### Create a New Case
```
# File → New Case
# Enter Case Name: Deleted_File_Recovery
# Choose Base Directory: C:\Cases\Deleted_File_Recovery
# Click Finish
```
### Add Disk Image
```
# Add Data Source → Disk Image or VM File
# Browse to: C:\forensics\disk.dd
# Click Next
```
### Run Ingest Modules
```# Select:
# - File System Analysis
# - Keyword Search (optional)
# - Data Recovery / Carving
# Click Finish
```
### Locate Deleted Files
```
# Navigate to 'Deleted Files' section in the tree view
# Review metadata (size, hash, timestamps)
```
### Export Deleted Files
```
# Right-click → Extract File(s)
# Save to: C:\forensics\Recovered_Files\
```

## OUTPUT:
Recovered Deleted File List and Details

<img width="1920" height="1080" alt="Screenshot (328)" src="https://github.com/user-attachments/assets/a209d857-9609-4446-8a49-70245c35dee4" />

<img width="1920" height="1080" alt="Screenshot (329)" src="https://github.com/user-attachments/assets/0d5b90f9-d73e-44b0-a257-4b9997ff54b7" />

<img width="1920" height="1080" alt="Screenshot (330)" src="https://github.com/user-attachments/assets/0dd3807e-5d47-4f1f-a927-a71d378839c5" />

<img width="1920" height="1080" alt="Screenshot (331)" src="https://github.com/user-attachments/assets/b9b8137d-d82a-4c15-b618-3705cbb8c5b8" />

<img width="1920" height="1080" alt="Screenshot (332)" src="https://github.com/user-attachments/assets/913898d2-f08d-4be1-98ed-64a4ecbb062d" />

<img width="1920" height="1080" alt="Screenshot (333)" src="https://github.com/user-attachments/assets/02e25a49-5b6f-472d-9423-7503ef25a0bd" />

<img width="1920" height="1080" alt="Screenshot (334)" src="https://github.com/user-attachments/assets/80826369-1eef-426b-aa7d-69061327c750" />








## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
