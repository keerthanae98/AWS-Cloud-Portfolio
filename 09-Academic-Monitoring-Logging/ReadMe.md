# Week 9 – Cloud Monitoring and Logging (CloudWatch & CloudTrail)

## 🔍 Objective
To create a monitoring dashboard and enable logging for academic bucket activity, enhancing observability and audit capability across services.

---

## 📊 CloudWatch Dashboard: `aca-resp-MCR-kee`
- **Metrics Tracked:**
  - `BucketSizeBytes`
  - `ResourceUsage`
- **Alert Setup:** `aca-adm-alarm-kee` configured to notify if usage thresholds are breached.
- **Time Range:** Custom (3 Months)
- 
<img width="959" alt="image1" src="https://github.com/user-attachments/assets/8730c924-570c-4061-b03a-41a81de50265" />

---

## 📋 CloudTrail Logging
- **Trail Name:** `aca-resp-trail-kee`
- **Trail Logging:** Enabled ✅
- **Multi-region Trail:** Yes
- **S3 Log Location:** 

<img width="959" alt="image2" src="https://github.com/user-attachments/assets/95025b4c-ed41-47eb-9ec1-48545a5ef7b9" />
