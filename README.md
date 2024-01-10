# AWS Rekognition-Based Face Recognition Service

This project demonstrates the creation of an advanced facial recognition system using Amazon Rekognition. It integrates several AWS services, including S3 for storage, Lambda for serverless computing, and DynamoDB for database management, to build a robust face login and registration system. This system exemplifies the efficient use of cloud technologies to create innovative solutions.

## Features
- **AWS Rekognition**: Utilizes advanced facial recognition capabilities.
- **AWS S3 Integration**: Leverages S3 for efficient image storage.
- **Serverless Architecture**: Employs AWS Lambda for streamlined application performance and reduced server management.
- **DynamoDB**: Utilizes DynamoDB for efficient data storage and retrieval.

## System Architecture
The system integrates various AWS services to create a seamless face recognition solution. AWS Lambda forms the backbone of the system, providing a serverless architecture that reduces the need for traditional server management. AWS S3 is used for storing facial images, and DynamoDB is employed for efficient data handling and management.

# Code Description
## Dependencies
  - boto3
  - decimal
  - json
  - urllib

## Key Components

1. **AWS Lambda Handler (lambda_handler)**: Acts as the main function triggered by AWS Lambda. It processes S3 event data to manage face recognition tasks.
2. **Index Faces (index_faces)**: Calls the Amazon Rekognition IndexFaces API to detect and index faces from images stored in S3.
3. **Update DynamoDB Index (update_index)**: Updates the DynamoDB table with face recognition data (FaceId and FullName).
4. **S3 Image Upload Script**: Iterates through a list of images and uploads them to the S3 bucket with associated metadata.

## AWS IAM Policy
The included IAM policy provides the necessary permissions for Lambda functions, including access to S3 objects, DynamoDB item updates, and face indexing through Rekognition.

## Setup and Deployment
1. **AWS Configuration**: Ensure all AWS services (Rekognition, S3, Lambda, DynamoDB) are configured properly.
2. **Deploy Lambda Function**: Upload the provided Lambda function code to AWS Lambda.
3. **Configure S3 Bucket**: Set up an S3 bucket for storing facial images.
4. **Set Up DynamoDB**: Create a DynamoDB table for data management.
5. **IAM Role Setup**: Ensure the Lambda function has the attached IAM policy for necessary permissions.
6. **Upload Images to S3**: Use the provided script to upload images to S3 for indexing.

## Usage
  - **Face Registration**: Upload a face image to the S3 bucket. The Lambda function will automatically index the face and store the data in DynamoDB.
  - **Face Login System**: Utilize the indexed data for facial recognition-based login systems.
