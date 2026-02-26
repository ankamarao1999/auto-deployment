Project: React Login App with GitHub Actions Deployment
🔹 Project Overview

This project contains a simple React login form and a CI/CD pipeline using GitHub Actions to deploy the app to Azure Web App or a Docker registry/AKS cluster.

📝 Features

Simple React login form with email and password.

Validates input fields.

GitHub Actions workflow for automatic deployment:

Build React app

Deploy to Azure Web App

Optional: Docker image push to Azure Container Registry (ACR)

🛠️ Prerequisites

Node.js >= 18

npm >= 8

GitHub repository

Azure subscription (for deployment)

Optional: Docker & Azure Container Registry (ACR) if deploying via container

⚡ Project Setup
1. Clone the repository
git clone https://github.com/<YOUR_USERNAME>/<YOUR_REPO>.git
cd <YOUR_REPO>
2. Install dependencies
npm install
3. Run locally
npm start

The app will run on http://localhost:3000

You should see the login form.

📂 Project Structure
src/
 └── components/
      └── LoginForm.jsx    # React login form component
.github/
 └── workflows/
      └── deployment.yaml # GitHub Actions workflow for CI/CD
⚙️ GitHub Actions Deployment
1. Create workflow file

.github/workflows/deployment.yaml

2. Configure secrets in GitHub

AZURE_CREDENTIALS – JSON credentials for Azure login

AZURE_WEBAPP_PUBLISH_PROFILE – Azure publish profile for the app

3. Workflow triggers

Push to main branch

Manual workflow dispatch

4. Workflow steps

Checkout code

Setup Node.js

Install dependencies

Build React app

Login to Azure

Deploy to Azure Web App

Optional: Build & push Docker image to ACR

📌 Notes

Update <YOUR_APP_NAME> in deployment.yaml to match your Azure Web App.

If using Docker/AKS, configure your registry credentials in GitHub secrets.

For custom styling, modify LoginForm.jsx.
