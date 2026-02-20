# Azure Blob Storage 

This project demonstrates the fundamentals of Azure Blob Storage with a focus on
basic security concepts relevant to the AZ-900 (Microsoft Azure Fundamentals) exam.

## Objective
- Understand Azure Blob Storage as an object storage service
- Learn how access to blobs is controlled
- Apply basic security practices using private containers and SAS tokens
- Understand shared responsibility in Azure PaaS services

---

## Architecture Overview
- Azure Storage Account (Standard, LRS)
- Private Blob Container
- Blob objects (PDF files)
- Access controlled using Shared Access Signatures (SAS)

---

## Steps Performed

### 1. Create a Storage Account
- Performance: Standard
- Replication: Locally Redundant Storage (LRS)
- Secure transfer required: Enabled
- Public blob access: Disabled

<img width="1919" height="996" alt="Screenshot 2026-02-19 210530" src="https://github.com/user-attachments/assets/334bb372-ca28-4686-b63b-82167766aad8" />

  

### 2. Create a Private Blob Container
- Container access level set to **Private**
- Prevented anonymous access to stored data

<img width="1919" height="898" alt="Screenshot 2026-02-20 180309" src="https://github.com/user-attachments/assets/d6b15624-a080-4c8a-b8e8-f1800cdb06df" />


### 3. Upload Files
- Uploaded sample PDF files to the container
- Verified blob URLs are not accessible without authentication

<img width="1919" height="768" alt="Screenshot 2026-02-20 180347" src="https://github.com/user-attachments/assets/6f50dfba-93cb-4f5a-89bf-577720411304" />


### 4. Test Access Control
- Attempted direct blob access (failed as expected)
- Generated a **Read-only SAS token** with a short expiry
- Accessed blob successfully using the SAS URL
- Verified access is revoked after SAS expiry

Access rejected
<img width="1288" height="331" alt="Screenshot 2026-02-20 180736" src="https://github.com/user-attachments/assets/a47653e5-e3c2-4154-9748-9e6a06e08ca0" />

Access using SAS URL
<img width="1919" height="664" alt="Screenshot 2026-02-20 181133" src="https://github.com/user-attachments/assets/2e8f2823-44d9-49a7-b87d-d827fb49744d" />

---

## Key Learnings
- Azure Blob Storage is used for storing unstructured data as objects
- Blob URLs do not imply public access
- SAS tokens provide time-limited and permission-scoped access
- Azure secures the infrastructure, while access control is the customer’s responsibility

---

## Technologies Used
- Microsoft Azure
- Azure Blob Storage
- Shared Access Signatures (SAS)

---

