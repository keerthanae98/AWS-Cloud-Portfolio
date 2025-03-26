# Week 8 – Academic Quality Check & Conditional Routing with AWS Glue

## 🧠 Project Overview
This project demonstrates the creation of a data quality check and conditional routing workflow using AWS Glue Studio. The goal was to process a dataset, perform a quality check, and route the data to separate S3 folders based on the result.

---

## 🔧 Tools & Services Used
- **AWS Glue Studio** – to build and manage the ETL workflow visually.
- **Amazon S3** – to store input and output datasets.
- **AWS IAM** – for permission management during job execution.

---

## 🔁 Workflow Summary

### 1. **Data Ingestion**
- Source file loaded from an S3 bucket.
- Dataset: `faculty member list`.

### 2. **Data Quality Check**
- A transformation step named `QC Check` evaluated data quality.
- Followed by a selection of rows using `rev&evalOutcomes`.

### 3. **Routing Logic**
- A **Conditional Router** node directed the data flow based on quality.
  - **If Quality Passed**:
    - Applied schema transformation and prepared for load.
    - Loaded into S3 path:  
      `s3://academics-trf-kee/responsibilities/facultymember-list/Quality check/Passed/`
  - **If Quality Failed (Default Group)**:
    - Same schema applied.
    - Loaded into S3 path:  
      `s3://academics-trf-kee/responsibilities/facultymember-list/Quality check/Failed/`
<img width="959" alt="image1" src="https://github.com/user-attachments/assets/8003245f-54ff-4b53-bf4c-e0ff9e94d887" />

---

## ✅ Output

### ✔️ Passed Folder
- File: `run-1741397924884-part-r-00000`
- Last Modified: March 7, 2025
- Size: 3.5 KB

  <img width="959" alt="image2" src="https://github.com/user-attachments/assets/b19b4c46-074a-4793-a31c-b5484e96256a" />


### ❌ Failed Folder
- File: `run-1741397909514-part-r-00000`
- Last Modified: March 7, 2025
- Size: 3.0 KB
<img width="959" alt="image3" src="https://github.com/user-attachments/assets/8d825617-75fc-4c74-9b31-56eac5a8ceb7" />

---

## 📊 Key Concepts Practiced
- Data quality validation
- Conditional routing logic
- Schema transformation
- S3 integration in Glue
- Job visualization & flow design in AWS Glue Studio

---

## 📅 Last Modified
**March 7, 2025**

