# 📁 Week 2 – Academic Dataset Ingestion using Amazon S3

## 📝 Objective:
To upload and organize academic CSV datasets into Amazon S3 using structured folders and access via internet-connected academic teams.

---

## 🧰 AWS Services Used:
- **Amazon S3** – For storing CSV files
- **AWS CLI (via PowerShell)** – For uploading files with folder structures
- **S3 Bucket Folder Structure** – To organize datasets by year, type, and server

---

## 🧪 What I Did:
- Collected 3 academic CSV files:
  - `faculty-member-list.csv`
  - `scholarlyactivity-list.csv`
  - `activitycommitteemembers-list.csv`
- Created the folder path in S3: responsibilities/facultymember-list/year-2025/server=AGVS-Kee/
- Used PowerShell + `Write-S3Object` command to upload each file.
- Verified successful upload using the S3 web console.

---

## 📸 Screenshots:
- 📁 Folder structure in S3
- 📄 CSV schemas (ERD)
- ⚙️ CLI commands & errors
- ✅ Final upload confirmation in S3

---

## 🧠 Learnings:
- Got hands-on with CLI-based upload.
- Understood folder-based key structuring in S3.
- Practiced organizing semi-structured data in buckets.

---

## 🔗 Project Files:
- All screenshots and CSV files are available in this folder.
