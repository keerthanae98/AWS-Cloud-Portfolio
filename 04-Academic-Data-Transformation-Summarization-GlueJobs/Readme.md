# 📊 Academic Dataset Transformation & Summarization – AWS Glue Jobs (Week 4)

This module showcases how AWS Glue was used to transform, summarize, and organize academic datasets stored in S3. Using **Visual ETL in AWS Glue Studio**, three summarization jobs were created for:

- Faculty Member List
- Scholarly Activity List
- Activity Committee Members List

---

## 🔧 Services Used
- **Amazon S3** – Data Lake storage
- **AWS Glue Studio** – Visual ETL job creation
- **AWS Glue Data Catalog** – Table management
- **Parquet Format** – For optimized storage

---

## 🧩 Folder Structure

| Folder Name         | Description |
|---------------------|-------------|
| `GlueJobs/`         | Visual ETL screenshots for each transformation job |
| `S3-Outputs/`       | Output files in Parquet format, stored under separate folders in S3 |
| `GlueDataCatalog/`  | Final registered tables in the AWS Glue Data Catalog |
| `ETL-Jobs-List/`    | Summary screenshot showing all 3 ETL jobs in AWS Glue Studio |

---

## ✅ Summary of Jobs

| Job Name | Input Dataset | Output Stored In | Output Format |
|----------|----------------|------------------|----------------|
| `facultymember-list-Summarization` | faculty.csv | `s3://.../faculty/` | Parquet |
| `scholarlyactivity-list-Summarization` | scholarly.csv | `s3://.../scholarlyactivity/` | Parquet |
| `activitycommitteemembers-list-Summarization` | committee.csv | `s3://.../activitycommitteemembers/` | Parquet |

---

## 📌 Outcome

All three jobs were executed successfully. Clean and structured Parquet files were generated and registered in the Glue Data Catalog for querying and analysis.

