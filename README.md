# expert-octo-doodle

# Todo Application

Frontend URL : (https://victorious-water-0e737791e.5.azurestaticapps.net/)

Backend URL : (https://newbe101.azurewebsites.net/)

## Description
This project is a simple Todo application consisting of a Node.js backend and a ReactJS frontend. It uses Azure DevOps for CI/CD, deploying the backend to Azure App Service and the frontend to Azure Static Web Apps.

## Table of Contents
- [Setup and Run Locally](#setup-and-run-locally)

### Backend (Node.js)

1. **Clone the repository**:
   ```sh
    git clone https://github.com/tracie96/expert-octo-doodle.git 

cd todo_be for backend
cd todo_fe for frontend


2. **Install Dependencies**:
   ```sh
   yarn install (i love using yarn :)

3. **Start Server**:
   ```sh
   node app.js or nodemon


### Frontend (React.js)

1. **Clone the repository**:
   ```sh
   git clone https://github.com/tracie96/todoFE
   cd todoFE

2. **Install Dependencies**:
   ```sh
   yarn install

3. **Start Server**:
   ```sh
   yarn start

![Application Screenshot](https://res.cloudinary.com/tracysoft/image/upload/v1719010312/Screenshot_2024-06-21_at_11.48.49_PM.png)


### I added tests

1. **To run**:
   ```sh
    yarn test

### CI/CD Pipeline Configuration


1. **Backend Pipeline**:
    - The backend pipeline (azure-pipelines-backend.yml) performs the following tasks:
    - Trigger: The pipeline triggers on any changes to the main branch and on pull requests.
    Steps:
    - Checkout Code: Checks out the repository code.
    - Set up Node.js: Sets up the Node.js environment.
    - Install Dependencies: Installs project dependencies using npm install.
    - Create Zip Artifact: Creates a zip file of the entire project for deployment.
    - Upload Artifact: Uploads the created zip file to be used in the deployment job.
    - Download Artifact: Downloads the artifact in the deployment job.
    - Unzip Artifact: Unzips the artifact to prepare for deployment.
    - Login to Azure: Logs in to Azure using the provided credentials from GitHub Secrets.
    - Deploy to Azure Web App: Deploys the unzipped artifact to the specified Azure Web App.Deploy to Azure Web App: Deploys the unzipped artifact to the specified Azure Web App.

1. **Frontend Pipeline**:
    - The frontend pipeline (azure-pipelines-frontend.yml) performs the following tasks:
    - Trigger: The pipeline triggers on any changes to the main branch and on pull requests.
    Steps:
    - Checkout Code: Checks out the repository code.
    - Set up Node.js: Sets up the Node.js environment.
    - Install Dependencies: Installs project dependencies using npm install.
    - Build Application: Builds the ReactJS application.
    - Deploy to Azure Static Web Apps: Deploys the built application to Azure Static Web Apps.


  