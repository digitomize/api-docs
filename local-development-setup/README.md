# ⚙ Local Development Setup

In this page, there will be instructions on how to locally setup your development environment

## Prerequisites

You will need the following installed on your system:&#x20;

* Node/NPM&#x20;
* Git&#x20;
* Code editor of your choice

## Setting up a development environment

1. Clone the Digitomize repository

```sh
git clone https://github.com/digitomize/digitomize.git
```

2. Install all the dependencies in the root directory

```sh
npm install
```

3. Configure the environment variables for the client directory and the backend directory.&#x20;

Use the following guides to help you setup and configure all the requirements.

<table data-card-size="large" data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td></td><td>Frontend Setup</td><td></td><td><a href="frontend-setup.md">frontend-setup.md</a></td></tr><tr><td></td><td>Backend Setup</td><td></td><td><a href="backend-setup.md">backend-setup.md</a></td></tr></tbody></table>

### Running the Application

Once all the environment variables are setup, you can start the development server.

```sh
npm run dev
```

This command will start both the frontend and backend servers.

Congratulations. That's it!🎉&#x20;

You're all setup and ready to interact with the project.
