# AWS Lambda S3 Image Resizer (Serverless)

## 📌 Overview
This project demonstrates an **Event-Driven Architecture** using AWS. When an image is uploaded to a specific S3 bucket, an AWS Lambda function is triggered to process the image and move it to a destination bucket.

## 🛠 Tech Stack
*   **Cloud:** AWS (S3, Lambda, IAM, CloudWatch)
*   **Language:** Python 3.x
*   **Library:** Boto3 (AWS SDK)

## 🚀 Workflow
1.  **S3 Source Bucket:** Receives the original image upload.
2.  **S3 Trigger:** Detects the `s3:ObjectCreated:*` event.
3.  **AWS Lambda:** Executes Python code to retrieve the image.
4.  **S3 Destination Bucket:** Stores the processed version of the image.

## ⚙️ Setup & Configuration
1.  Created two S3 buckets: `source` and `destination`.
2.  Configured an **IAM Role** with `AmazonS3FullAccess` and `CloudWatchLogsFullAccess`.
3.  Added an **S3 Trigger** to the Lambda function.
4.  Deployed the Python script using the AWS Lambda Console.

## 📈 Future Improvements
*   Add **AWS Lambda Layers** to include the `Pillow` library for actual image resizing.
*   Implement **SNS Notifications** to alert the user when processing is complete.
