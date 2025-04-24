# 🚀 Automated Receipt Processing Tool

### ⏱️ Deployment Time: 30–60 minutes | 🔓 Available under AWS Free Tier

Welcome to the **Automated Receipt Processing Tool**! This project is designed to automate the tedious and error-prone process of entering receipt data manually. Leveraging the power of AWS cloud services, this tool extracts key information from receipt images and stores it efficiently in the cloud. Whether you’re working on personal projects or looking for an automated solution for receipt tracking, this is your go-to tool!

---

## 🧠 Project Overview

In today’s fast-paced world, businesses and individuals spend a significant amount of time managing and organizing receipts. From keeping track of expenses to categorizing purchases, the process can be repetitive and time-consuming. **The Automated Receipt Processing Tool** is here to streamline that process.

**Goal:**  
Create a serverless solution that automatically processes receipts by extracting data such as vendor name, date, total amount, and item details from receipt images. The data is then stored in a database and users are notified via email once the process is complete.

---

## 🔧 How It Works

1. **Upload a Receipt:**  
   A user uploads an image or PDF of a receipt to an **Amazon S3** bucket.

2. **Automated Processing:**  
   The S3 upload event triggers an **AWS Lambda** function, which invokes **Amazon Textract** to perform OCR on the receipt.

3. **Data Extraction:**  
   **Amazon Textract** extracts vendor name, date, total amount, and line-item details from the receipt image.

4. **Store the Data:**  
   Extracted information is stored in **Amazon DynamoDB** in a structured format for fast, reliable retrieval.

5. **Email Confirmation:**  
   Upon successful processing, **Amazon SES** sends an email summarizing the extracted data back to the user.

---

## 🧰 Technologies Used

| Service             | Purpose                                                    |
|---------------------|------------------------------------------------------------|
| **Amazon S3**        | Secure storage for uploaded receipt files (JPG, PNG, PDF) |
| **Amazon Textract**  | OCR to extract structured data from receipts               |
| **AWS Lambda**       | Serverless compute to trigger document processing          |
| **Amazon DynamoDB**  | NoSQL database to store receipt metadata                   |
| **Amazon SES**       | Sends email notifications with receipt summaries           |
| **AWS IAM**          | Manages fine-grained access control to AWS resources       |

---

## 🧠 Key Features

- 📥 **Easy Upload:** Upload receipts in JPG, PNG, or PDF formats to S3.  
- ⚡ **Serverless Processing:** Lambda and Textract automate extraction without managing servers.  
- 🧾 **Accurate OCR:** Textract parses vendor, date, total, and items with high accuracy.  
- 📊 **Structured Storage:** DynamoDB stores all metadata for easy querying.  
- 📧 **Instant Notifications:** SES emails a summary of each processed receipt.  
- 🔐 **Secure by Design:** IAM roles enforce least-privilege access across services.  

---

## 🎯 Outcomes & Benefits

This tool is designed to save time, reduce human error, and provide an efficient solution for receipt management.

- **Eliminates Manual Entry:** No more typing out vendor names, amounts, or dates.  
- **Time-Saving:** Scans and processes receipts in minutes instead of hours.  
- **Cost-Effective:** Fully serverless—only pay for what you use. Ideal for personal or small business use.  
- **Scalable:** Easily handle an unlimited number of receipt uploads as your needs grow.  

---

## 🔑 Security & Access Management

Using **AWS IAM (Identity and Access Management)** roles and policies, this project ensures that only authorized users and services have access to the resources involved in the receipt processing pipeline.

---

## 💡 Lessons Learned

Working on this project helped me deepen my understanding of:

- AWS serverless services and event-driven architectures.  
- Integrating **Amazon Textract** for document analysis and OCR.  
- Building a seamless, end-to-end pipeline using S3, Lambda, DynamoDB, and SES.  
- Applying IAM best practices to secure interactions between services.  

---

Connect with me on [LinkedIn](https://www.linkedin.com/in/khushi-nandwani/), let’s spark new ideas together!
