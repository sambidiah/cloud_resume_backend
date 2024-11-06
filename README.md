# Cloud Resume Backend

## Project Summary
This repository contains the backend API code for the Cloud Resume Challenge. It includes an AWS Lambda function and API Gateway configuration to manage the visitor counter for the resume frontend.

## Project Overview
The backend supports the frontend’s visitor counter by using an API to interact with a DynamoDB table. This setup allows the resume page to display an updated visitor count on each visit.

## Key Files and Directories
- **`lambda_function.py`**: Python code for the Lambda function that processes API requests to update and retrieve the visitor count.
- **`tests/`**: Contains test files to verify the functionality and reliability of the Lambda function.

## API Details
The backend API exposes the following endpoints:
- **GET /visitor-count**: Retrieves the current visitor count from DynamoDB.
- **POST /visitor-count**: Increments and updates the visitor count in DynamoDB.

## Testing
Automated tests verify the backend’s functionality:
- **Unit Tests**: Validate core logic of the Lambda function.
- **System Tests**: Confirm interactions with DynamoDB.
- **End-to-End Tests**: Ensure the API behaves as expected when called by the frontend.

## Deployment on AWS
1. **Lambda Function**: The visitor counter logic is implemented in Python and deployed to AWS Lambda.
2. **DynamoDB Table**: Stores visitor count data.
3. **API Gateway**: Exposes the Lambda function as a REST API for communication with the frontend.

## CI/CD Workflow
This repository includes a GitHub Actions workflow for CI/CD:
- **Testing**: Runs automated tests on code pushes.
- **Deployment**: Deploys updates to AWS Lambda if all tests pass.

## Additional Information
- **Security**: IAM roles restrict Lambda function access, ensuring secure handling of data.
- **Error Handling**: The Lambda function includes error handling to manage unexpected issues during API requests.
