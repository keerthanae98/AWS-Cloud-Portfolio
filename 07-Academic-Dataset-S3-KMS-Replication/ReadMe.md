# Week 7 – Academic Dataset: S3 KMS Encryption, Versioning & Replication

This week focused on securing academic datasets using **AWS KMS**, enabling **bucket versioning**, and configuring **replication rules** for durability and compliance.

---

## 🔐 KMS Key Configuration

A customer-managed symmetric key was created to encrypt academic data across buckets.

- **Key alias:** `academics-resp-key-kee`
- **Key spec:** SYMMETRIC_DEFAULT
- **Usage:** Encrypt and decrypt
- **Status:** Enabled

<img width="959" alt="image1" src="https://github.com/user-attachments/assets/29f599a3-1880-4441-95b4-96cf367d7ea1" />


---

## 🪣 S3 Buckets Configured with KMS + Versioning

### 1. academics-raw-kee
- Encryption: SSE-KMS using the key above
- Bucket Key: Enabled
- Versioning: Enabled

<img width="959" alt="image2" src="https://github.com/user-attachments/assets/2889957e-ec68-4d92-8dca-c8abeb67e17d" />

<img width="959" alt="image3" src="https://github.com/user-attachments/assets/9a09ce2c-3971-4bab-b5d8-f86fe4298ea3" />

---

### 2. academics-cur-kee
- Encryption: SSE-KMS using the same key
- Bucket Key: Enabled
- Versioning: Enabled

<img width="959" alt="image6" src="https://github.com/user-attachments/assets/92711d83-bf5a-4a01-96ec-8bd503c44a99" />
<img width="959" alt="image7" src="https://github.com/user-attachments/assets/44e68869-99c2-4909-9867-c3254b3cd27d" />


---

### 3. academics-trf-kee
- Encryption: SSE-KMS using the same key
- Bucket Key: Enabled
- Versioning: Enabled

<img width="959" alt="image9" src="https://github.com/user-attachments/assets/f1ef54f8-49aa-466e-9f9c-db47a79552ee" />

<img width="959" alt="image10" src="https://github.com/user-attachments/assets/20a68452-7c98-41df-8366-6a10b5b1667e" />

---

## 🔁 Replication Rules Set Up

Each primary bucket has cross-bucket replication configured:

- **academics-raw-kee → academics-raw-backup-kee**  
<img width="959" alt="image4" src="https://github.com/user-attachments/assets/aa6ee2f7-2afd-4763-ac70-5e2414cebc37" />


- **academics-cur-kee → academics-cur-backup**  
<img width="959" alt="image8" src="https://github.com/user-attachments/assets/c701b9de-88f9-4cb6-a1c4-fcc39c108e7d" />




> Replication was configured for:
> - Entire bucket
> - KMS-encrypted objects replication: Enabled
> - Replication time control: Disabled
> - Replica modification sync: Disabled

---

## ✅ Summary

This week’s task helped me:
- Create & apply a secure KMS key for S3 encryption
- Implement bucket versioning to preserve data history
- Set up reliable replication rules for backup & recovery

---

