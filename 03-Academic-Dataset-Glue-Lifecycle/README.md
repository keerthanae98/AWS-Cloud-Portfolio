# 📚 Week 3 – Academic Dataset Ingestion, Analysis & Lifecycle Management

## 🔍 Overview

This project demonstrates the end-to-end pipeline for academic data ingestion, profiling, transformation, and lifecycle configuration using **AWS S3**, **AWS Glue DataBrew**, and **EC2**. The solution is built to simulate a scalable academic data analysis platform that ingests CSV datasets, transforms and profiles them using DataBrew, and manages cost-efficiency using intelligent storage and lifecycle rules.

---

## 📁 Datasets Used

| Dataset Name                     | File                          | Description                                  |
|----------------------------------|-------------------------------|----------------------------------------------|
| Faculty Member List              | `facultymember-list.csv`      | Faculty member details including experience. |
| Scholarly Activity List          | `scholarlyactivity-list.csv`  | Research publications and scholarly records. |
| Activity Committee Members List | `activitycommitteemembers-list.csv` | Committee member records for university activities. |

---

## 🧱 Architecture Summary

- Raw datasets ingested into: `academics-raw-kee`
- Transformed & profiled outputs saved to: `academics-trf-kee`
- Processing done via: **AWS Glue DataBrew**
- Output format: **CSV** and **Parquet** (with Snappy compression)
- Lifecycle policies applied for storage class transitions

---

## 📊 Data Profiling & Cleansing

All datasets were profiled using AWS Glue DataBrew to:
- Check for missing values
- Determine data types
- Identify correlations (e.g., `Years_of_Experience`)
- Cleanse and normalize data
- Output to S3 in CSV & Parquet

**Data Quality Summary**  
| Dataset                  | Total Rows | Total Columns | Missing Cells | Cleansing Job Status |
|--------------------------|------------|----------------|----------------|------------------------|
| Faculty List             | 50         | 11             | 0              | ✅ Succeeded           |
| Scholarly Activity       | 100        | 11             | 5%             | ✅ Succeeded           |
| Activity Committee List  | 50         | 10             | 0              | ✅ Succeeded           |

---

## 🔄 Lifecycle Rules Applied

Lifecycle policies were created on the `academics-raw-kee` bucket for each dataset to move infrequently accessed data to **Glacier/Glacier Instant Retrieval**, reducing storage cost over time.

| Lifecycle Rule Name              | Transition Target          |
|----------------------------------|-----------------------------|
| `academics-fm-lst-lr-kee`        | Glacier Instant Retrieval   |
| `academics-sha-lst-lr-kee`       | Glacier Flexible Retrieval  |
| `academics-acm-lst-lr-kee`       | Glacier Flexible Retrieval  |

---

## 🔐 Logs and Access Monitoring

- Server logs captured from EC2 Windows instance (`IIS` logs)
- Sample logs stored under `responsibilities/academics-user-log/year=2025/...`
- EC2 instance used PowerShell and `Write-S3Object` (note: required credentials setup to avoid failure)

---

## 🧠 Learnings and Outcomes

- Practical use of **DataBrew** for no-code profiling and transformation  
- Efficient storage with **S3 Lifecycle Rules**  
- Real-world simulation of academic data team ingestion pipelines  
- Use of **CSV and Parquet** formats for flexibility and compression  
- Error handling during PowerShell S3 uploads  

---

## 📌 Screenshots

All screenshots documenting each step are stored in this directory as `image1.png` to `image13.png`.

---

## ✅ Completion Status

| Task                                | Status      |
|-------------------------------------|-------------|
| S3 Bucket Creation                  | ✅ Done      |
| Data Upload (Raw)                   | ✅ Done      |
| Glue DataBrew Profiling             | ✅ Done      |
| Data Cleansing Job (CSV + Parquet) | ✅ Done      |
| Lifecycle Rules                     | ✅ Done      |
| Logs and EC2 CLI Execution          | ✅ Done      |
| Documentation and Diagram (draw.io) | ✅ Done      |

---

## 🔗 Output Paths

Example S3 output folder: s3://academics-trf-kee/responsibilities/facultymember-list/user/


Parquet output with compression:  s3://academics-trf-kee/responsibilities/facultymember-list/system/



---

## 👩‍💻 Created By

**Keerthana A.** – AWS Academy Cloud Foundations  
Project: Cloud Computing Portfolio – Week 3  
<img width="959" alt="image13" src="https://github.com/user-attachments/assets/591e0218-dada-4ba4-8df2-0aa4e04d175f" />
<img width="769" alt="image12" src="https://github.com/user-attachments/assets/596cbfde-784f-41e2-a384-848b3e158f5d" />
<img width="769" alt="image11" src="https://github.com/user-attachments/assets/bdeb2715-aac9-4cda-b242-08bb18fb3fa2" />
<img width="959" alt="image10" src="https://github.com/user-attachments/assets/1b72240f-fee4-4f6e-b2c6-b45990d01172" />
<img width="959" alt="image9" src="https://github.com/user-attachments/assets/2f51a05a-bc6b-4dfe-b7a5-4c26aec0aca4" />
<img width="959" alt="image8" src="https://github.com/user-attachments/assets/450570d3-8e4f-47ee-b733-402b06f70fa8" />
<img width="959" alt="image7" src="https://github.com/user-attachments/assets/0c5adda6-852e-4189-8fea-0b46c2cb0eb1" />
<img width="959" alt="image6" src="https://github.com/user-attachments/assets/0c20e82a-809f-4bd2-88c3-996760f2543d" />
<img width="959" alt="image5" src="https://github.com/user-attachments/assets/bdc08197-eee6-480f-ac3c-c535332697ad" />
<img width="959" alt="image4" src="https://github.com/user-attachments/assets/fc819539-2b01-4512-8803-7f2889449656" />
<img width="959" alt="image3" src="https://github.com/user-attachments/assets/0216baf1-8c53-4f26-b2d8-1aef92954309" />
<img width="959" alt="image2" src="https://github.com/user-attachments/assets/2923c29a-93e0-4eef-b954-fa0f309aa83f" />
<img width="959" alt="image1" src="https://github.com/user-attachments/assets/f28dddf6-beed-47b6-a26b-617b6d428ec3" />

