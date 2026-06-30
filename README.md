# Cloud Second Brain

An event-driven, serverless cloud application built on AWS that automatically ingests, analyzes, and organizes uploaded files (images, documents, screenshots) into a searchable personal knowledge base.

---

## 🚀 Overview

**Cloud Second Brain** is designed to solve the problem of digital clutter. Instead of manually organizing files into deep folder structures, this application leverages a serverless cloud architecture to process files dynamically upon upload. 

The primary architecture is built manually via the AWS Console to deeply understand the mechanics of each service, with a planned migration to Infrastructure as Code (Terraform) once the system is fully operational.

### Key Goals:
- **Zero Infrastructure Management:** Fully serverless architecture utilizing AWS Free Tier resources.
- **Event-Driven Execution:** File uploads immediately trigger processing pipelines without manual intervention.
- **AI-Ready Foundation:** Built to easily integrate intelligent OCR, face recognition, and LLM capabilities in future milestones.

---

## 🏗️ Architecture

Phone or Computer
        │
        ▼
 Upload File
        │
        ▼
[ Amazon S3 Bucket ]
        │
        ▼  (S3 Event Notification)
[ AWS Lambda Function ]
        │
        ▼  (Rule-Based/AI Classification)
   Generate Metadata
        │
        ▼
[ Amazon DynamoDB ]
        │
        ▼
  Search Later (Web UI)



---

## 🛠️ Tech Stack

* **Cloud Provider:** Amazon Web Services (AWS)
* **Storage:** Amazon S3
* **Compute:** AWS Lambda (Python 3.12)
* **Database:** Amazon DynamoDB
* **API Layer:** Amazon API Gateway
* **Security & Logging:** AWS IAM, Amazon CloudWatch


* **Backend Language:** Python
* **Frontend Framework:** React (Planned)
* **Infrastructure as Code:** Terraform (Planned Migration)

---

## 🗺️ Development Roadmap

* [x] **Milestone 1: Core Storage Foundation**
* Set up AWS environment and IAM permissions.
* Create secure S3 bucket with "Block Public Access" enabled.
* Test manual upload, retrieval, and access control policies.


* [ ] **Milestone 2: Serverless Compute Setup**
* Deploy first Python-based AWS Lambda function.
* Configure test events and master Amazon CloudWatch monitoring/logging.


* [ ] **Milestone 3: Event-Driven Integration**
* Connect S3 object creation notifications to Lambda triggers.
* Log automated extractions (filenames, metadata, execution timestamps).


* [ ] **Milestone 4: Metadata Persistence**
* Provision a DynamoDB NoSQL table.
* Update Lambda to store structured metadata (tags, categories, file types).


* [ ] **Milestone 5: Automated Logical Organization**
* Script Lambda to automatically route files into structured S3 logical prefixes (folders).


* [ ] **Milestone 6: Client-Side Ingestion Interface**
* Build a simple upload web interface using React to bypass the AWS console.


* [ ] **Milestone 7: Search and Discovery Interface**
* Implement a web interface to query DynamoDB and locate files by tags, dates, and names.


* [ ] **Milestone 8: Infrastructure as Code Migration**
* Replicate the entire verified architecture programmatically using Terraform.



---

## 📁 Repository Structure

```text
cloud-second-brain/
│
├── frontend/          # React Web Application (Future)
│
├── backend/           # Core Python helper modules
│
├── lambda/            # AWS Lambda function handlers
│   └── classify.py
│
├── terraform/         # Infrastructure as Code configuration (Future)
│
├── docs/              # Architectural diagrams and deep-dives
│   └── architecture.md
│
└── README.md

```

---

## 🔒 Security Best Practices Implemented

* **Principle of Least Privilege (PoLP):** IAM policies restrict Lambda and execution components to access only the specific buckets and tables required.
* **Private by Default:** S3 public access block rules prevent data leakage or unauthorized access via global Object URLs.

```

---

### What's Next?
Commit this file to your `cloud-second-brain` repository on GitHub. Once your repository is updated, we are ready to move on to **Milestone 2**: writing and deploying your first Python AWS Lambda function! Let me know when you are ready.

```
