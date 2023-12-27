---
description: Setting up the backend locally
---

# 🧑💻 Backend Setup

Once you have cloned the [Digitomize repository](https://github.com/digitomize/digitomize.git) and installed the dependencies in the root directory, you can take the following steps to setup the backend of the project.&#x20;

### 1. Navigate to the backend directory

```sh
cd digitomize/backend
```

### 2. Install all the dependencies

```sh
npm install
```

### 3. Get the Firebase App Credentials

You will be using the same Firebase App as the frontend or if you haven't already created a Firebase app, you can follow [these instructions](https://app.gitbook.com/o/ekMF9zG3tvNrhkhDZTBE/s/S29E4JrAA1b3pzZaElxO/\~/changes/10/quick-start/frontend-setup#3.-creating-a-firebase-project.).

To get the Firebase App credentials, you will need to:

1. select the project
2. go to the 'Project Overview' by clicking on the gear icon
3. choose the 'Project Settings' option
4. navigate to the 'Service Accounts' tab
5. click on 'Generate new private key'. This will generate a private key and automatically download a JSON file containing the app credentials. The downloaded JSON file will have the following structure:

```json
{
  "type": "service_account",
  "project_id": "your-project-id",
  "private_key_id": "your-private-key-id",
  "private_key": "-----BEGIN PRIVATE KEY-----\nYourPrivateKey\n-----END PRIVATE KEY-----\n",
  "client_email": "your-service-account-email@your-project-id.iam.gserviceaccount.com",
  "client_id": "your-client-id",
  "auth_uri": "https://accounts.google.com/o/oauth2/auth",
  "token_uri": "https://oauth2.googleapis.com/token",
  "auth_provider_x509_cert_url": "https://www.googleapis.com/oauth2/v1/certs",
  "client_x509_cert_url": "https://www.googleapis.com/robot/v1/metadata/x509/your-service-account-email%40your-project-id.iam.gserviceaccount.com"
}
```

### 4. Configuring the Environment Variables

To add the Firebase App credentials, you can take the folllowing steps:

1. Create a `.env` file
2. Copy the `.env.example` file or use the following template:

```json
TEST=Env file connected.
MONGODB_URL=mongodb://localhost:27017/digitomize
PORT=4001
BACKEND_URL=http://localhost:4001
CONTESTS=true
USERS=true
NODE_ENV=development

# Firebase Configuration
FIREBASE_CREDENTIALS= # you need to add JSON for this
```

3. Copy the downloaded JSON file into the `FIREBASE_CREDENTIALS` variable

### 5. Starting the Development Server

To ensure that the backend server is functional, you can try starting the server by running the following command

```sh
npm start
```

You are all setup. 🎉

To run the application, start both the frontend and backend by following [these instructions](./#running-the-application).
