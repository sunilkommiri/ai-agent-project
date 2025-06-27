**AI Agent Platform**
**Overview**
This project is a full-stack, serverless AI Agent application built on AWS. It provides a modern, chat-based interface inspired by Google's Gemini, allowing users to have interactive conversations with an AI powered by the Google Gemini API.

The agent is designed to be intelligent and stateful, capable of holding natural conversations, using tools like Google Search to answer questions, and remembering past conversations for a continuous user experience. The entire application is secured with user authentication.

**Features**
**Modern Chat UI:** A clean, responsive user interface built with HTML and Tailwind CSS, inspired by modern AI chat applications.

**Intelligent Agent:** The agent uses the Google Gemini API to understand and respond to user queries.

**Tool Use**: The agent can decide when it needs to use external tools (like Google Search) to find up-to-date information.

**P****ersistent Memory**: Conversations are saved on a per-user basis using Amazon DynamoDB, allowing for stateful, long-term interactions.

**Secure Authentication**: User sign-up and sign-in are handled by Amazon Cognito, and the backend API is protected, allowing access only to authenticated users.

**Serverless Architecture:** The entire backend is built on a scalable and cost-effective serverless architecture using AWS Lambda, API Gateway, and DynamoDB.

**CI/CD Deployment:** The front end is hosted on AWS Amplify and connected to this GitHub repository for continuous integration and deployment.

**Tech Stack
Front End**
HTML5
Tailwind CSS
JavaScript (ESM)
AWS Amplify JS Library

**Back End (Serverless)**
Compute: AWS Lambda (Node.js)

**API**: Amazon API Gateway (REST API)

**Database**: Amazon DynamoDB (NoSQL)

**Authentication**: Amazon Cognito

**AI Model:** Google Gemini API

**Deployment**
**Hosting & CI/CD**: AWS Amplify

**Setup and Deployment**
This project requires an AWS account and a Google AI Studio account to obtain a Gemini API key.

**Backend Setup (AWS):**

Phase 1: Secure Backend: Set up the AWS Lambda function and Amazon API Gateway as described in the development guide to create a secure endpoint and protect the Gemini API key.

Phase 2: Persistent Memory: Create the Amazon DynamoDB table and update the Lambda function's IAM role and code to enable conversation history.

Phase 3: Authentication: Create an Amazon Cognito User Pool and configure it as an authorizer for the API Gateway to secure the API.
**
Front-End Setup:**

Clone this repository.

Update the index.html file with your specific AWS resource details:

YOUR_USER_POOL_ID (from Cognito)

YOUR_APP_CLIENT_ID (from Cognito)

YOUR_AWS_REGION (e.g., us-east-1)

YOUR_API_GATEWAY_INVOKE_URL (from API Gateway)

Commit and push the changes to your GitHub repository.

Deployment (AWS Amplify):

Connect your GitHub repository to a new app in the AWS Amplify console.

Allow Amplify to automatically detect the build settings and deploy the application.

The application will be live at the URL provided by Amplify.
