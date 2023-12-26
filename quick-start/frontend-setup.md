---
description: Setting up the frontend locally
---

# Frontend Setup

Once you have cloned the [Digitomize repository](https://github.com/digitomize/digitomize.git) and installed the dependencies in the root directory. You can take the following steps to configure the frontend of the application.

### 1. Navigate to the client directory

```sh
cd digitomize/client
```

### 2. Install the dependencies for the frontend

```sh
npm install
```

### 3. Creating a Firebase project

You will need a Firebase application to get values for the environment variables. Create a firebase application by following these instructions:

1. Go to [Firebase](https://firebase.google.com/).
2. Create an account or log in to your existing account.
3. Add a project.
4. Add a web app
5. Add Firebase SDK to the web app

The `firebaseConfig` variable contains all the values required in the `.env` file.

```javascript
const firebaseConfig = {
  apiKey: "IKNdsaKsdabdGL5iuywrfHUIKBubkjbJGDfIBHUGnkjVA",
  authDomain: "sample-u78nb.firebaseapp.com",
  projectId: "sample-u78nb",
  storageBucket: "sample-u78nb.appspot.com",
  messagingSenderId: "872459742932",
  appId: "9:872459742932:web:&8ufnhjbhbj89nu8b",
  measurementId: "G-YTUTY89kFT",
};
```

### 4. Configure the environment variables

To add the Firebase configuration properties to the environment variables by:

1. Creating a `.env` file&#x20;
2. Copying the `.env.example` file or using this template

```
VITE_REACT_APP_BACKEND_URL=http://localhost:4001
VITE_REACT_APP_FRONTEND_URL=http://localhost:5173
VITE_REACT_APP_API_KEY=
VITE_REACT_APP_AUTH_DOMAIN=
VITE_REACT_APP_PROJECT_ID=
VITE_REACT_APP_STORAGE_BUCKET=
VITE_REACT_APP_MESSAGING_SENDER_ID=
VITE_REACT_APP_APP_ID=
VITE_REACT_APP_MEASUREMENT_ID=
```

### 5. Run the server.

To confirm that the frontend application is working, start the development server.

```sh
npm run dev
```

Yay! Your frontend application is working.🎉🎉

Next, you will setup the backend.
