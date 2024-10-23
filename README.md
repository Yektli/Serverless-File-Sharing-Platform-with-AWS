# Serverless-File-Sharing-Platform-with-AWS

### Project Summary:

This project implements a serverless file-sharing platform using Amazon Web Services (AWS) to provide a scalable, efficient, and cost-effective solution for file storage and sharing. The architecture leverages AWS services including S3 for file storage, API Gateway for routing requests, Lambda functions for backend logic, and DynamoDB for managing metadata.

The platform allows users to securely upload, download, and manage files without needing traditional server infrastructure. Key features include file versioning, secure access through presigned URLs, and scalable performance to handle variable user demands. The design prioritizes a pay-per-use model, reducing costs by only using resources as needed.

This approach highlights the strengths of serverless architectures by reducing operational overhead and eliminating the need for server maintenance, making it an efficient solution for modern cloud-based file sharing.



### Project Architecture:

![image](https://github.com/user-attachments/assets/29fdda0f-96e1-49a9-9b10-31af003366be)


### Development shown in steps:

1. An S3 bucket is set up as the primary storage location for the files uploaded by users.

2. Set Up Lambda Functions:
- UploadFunction: A Python-based AWS Lambda function that processes file uploads.
- DownloadFunction: Another Python Lambda function that handles file downloads.
Both functions are assigned an IAM role that grants write permissions to the S3 bucket.

3.API Gateway Creation: An API Gateway is set up to create two endpoints (POST and GET) that interact with the Lambda functions:
- POST /files: Used for uploading files.
- GET /files: Used for downloading files.

4. The POST and GET methods are configured to handle parameters and content correctly, including using Mapping Templates to ensure the API Gateway passes the necessary information to the Lambda functions.

5. The API is deployed to a specific stage (like "dev"), making it accessible for testing and use.

6. Postman or curl commands are used to test file uploads (using POST requests) and downloads (using GET requests), confirming that the platform works as intended.
