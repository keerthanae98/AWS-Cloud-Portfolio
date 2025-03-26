# Week 8 – Cloud Monitoring and Logging (CloudWatch & CloudTrail)

## 🔍 Objective
To create a monitoring dashboard and enable logging for academic bucket activity, enhancing observability and audit capability across services.

---

## 📊 CloudWatch Dashboard: `aca-resp-MCR-kee`
- **Metrics Tracked:**
  - `BucketSizeBytes`
  - `ResourceUsage`
- **Alert Setup:** `aca-adm-alarm-kee` configured to notify if usage thresholds are breached.
- **Time Range:** Custom (3 Months)
<img width="452" alt="Picture1" src="https://github.com/user-attachments/assets/80697edc-fff4-49f7-ac51-8be33d3cae3c" />

---

## 📋 CloudTrail Logging
- **Trail Name:** `aca-resp-trail-kee`
- **Trail Logging:** Enabled ✅
- **Multi-region Trail:** Yes
- **S3 Log Location:** 
