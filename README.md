# Serverless-File-Sharing-Platform-with-AWS

### Project Summary:

This project implements a serverless file-sharing platform using Amazon Web Services (AWS) to provide a scalable, efficient, and cost-effective solution for file storage and sharing. The architecture leverages AWS services including S3 for file storage, API Gateway for routing requests, Lambda functions for backend logic, and DynamoDB for managing metadata.

The platform allows users to securely upload, download, and manage files without needing traditional server infrastructure. Key features include file versioning, secure access through presigned URLs, and scalable performance to handle variable user demands. The design prioritizes a pay-per-use model, reducing costs by only using resources as needed.

This approach highlights the strengths of serverless architectures by reducing operational overhead and eliminating the need for server maintenance, making it an efficient solution for modern cloud-based file sharing.



### Project Architecture:

![image](https://github.com/user-attachments/assets/29fdda0f-96e1-49a9-9b10-31af003366be)


### Project Files:
The code employed for this project has been uploaded to this repository, it contains:

* Lambda Upload Code (UploadFunction.py): The function that handels files uploads to an S3 Buckect.
* Lambda Download Code (DownloadFunction.py): The function that handles files downloads from an Amazon S3 bucket.
* IAM Policy (iam_policy.json): This code represents an AWS Identity and Access Management (IAM) policy, designed to provide fine-grained access control to an S3 bucket.
