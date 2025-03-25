# Week 7 – Academic Dataset: S3 Bucket Encryption, Versioning & Replication with KMS

This week focused on securing and replicating S3 data using **AWS KMS**, **Bucket Versioning**, and **Cross-Bucket Replication**. The goal was to implement data durability and security across all academic datasets (RAW, CUR, TRF).

---

## 🔐 KMS Key Created

- **Key Alias:** `academics-resp-key-kee`
- **Key ID:** f77db36c-a80c-4370-9483-b566377e3f9b
- **Type:** Symmetric | Enabled | Encryption & Decryption

📸 `kms-key.png`

---

## 📁 Bucket Configurations (RAW, CUR, TRF)

Each bucket (raw, cur, trf) had the following enabled:

- ✅ **Server-side Encryption (SSE-KMS)** with the custom key
- ✅ **Bucket Key:** Enabled (reduces encryption cost)
- ✅ **Bucket Versioning:** Enabled

📸 Screenshots:
- `raw-encryption.png`
- `cur-encryption.png`
- `trf-encryption.png`

---

## 🔁 Replication Rules Setup

- Each primary bucket (raw, cur, trf) was configured with **replication rules** to a corresponding backup bucket.
- Replication was set for the **entire bucket**
- KMS-encrypted objects: ✅ Replicate
- Replication time control: ❌ Disabled (not needed)
- Modification sync: ❌ Disabled

📸 Screenshots:
- `raw-replication.png`
- `cur-replication.png`
- `trf-replication.png`

---

## 🧠 Reflections

✅ This task enhanced my understanding of:
- AWS KMS key creation and usage
- How S3 encryption works at scale using SSE-KMS
- Data durability using S3 **versioning** and **replication**
- Real-world application of security best practices

---

## 📸 Screenshot Summary

All screenshots are in `/week7-screenshots/`:
- `kms-key.png`
- `raw-encryption.png` / `raw-replication.png`
- `cur-encryption.png` / `cur-replication.png`
- `trf-encryption.png` / `trf-replication.png`
