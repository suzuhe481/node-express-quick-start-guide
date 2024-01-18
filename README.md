# Quick Start Guide for Node.js Express Apps

I created this guide to help me when starting a new Express app. I took note of the starting steps needed as well as some helpful packages/middlewares.

## Getting Started

- This guide assumes you understand how Node.js and Express applications work, and you just need help with the initial set up.
- The following instructions are assuming you are using the Linux OS. I use Ubuntu.
- Make sure to have the LTS (Long Term Support) of Node to avoid errors.

## Table of Contents

1. [Prerequisite](#1-prerequisite)
2. [Creating the App](#2-creating-the-app)
3. [Packages](#3-packages)
4. [Middleware](#4-middleware)

## [1] Prerequisite

- Install Express Application generator globally so you can create Express apps.

```
npm install express-generator -g
```

## [2] Creating the App

- Deciding on a template library for your project such as EJS, Pug(Jade), Hbs, etc.

- Open a terminal instance in the directory you want to create your project folder and run the following command replacing VIEW_TEMPLATE with the template you will use.

```
express my-first-express-app --view=VIEW_TEMPLATE
```

- E.g. If I wanted to create an app named _super-cool-app_ using the EJS template, I would run...

```
express super-cool-app --view=ejs
```

- This creates an Express app with some folders, an app.js and package.json files.

- **NOTE**: _For the following steps, I will assume the app's name is *super-cool-app*._

- Follow the termianl instructions to go to the project directory, install packages, and run the app.

```
cd super-cool-app
npm install
DEBUG=super-cool-app:* npm start
```

## [3] Packages

Here are some helpful packages you can use for your React projects.

### [nodemon](https://www.npmjs.com/package/nodemon)

- Automatically restarts the Node.js application when there are file changes.

```
npm install --save-dev nodemon
```

- Additionally, go to your package.json file and edit the scripts to the following, replacing the app name below with your app name.

```
"scripts": {
    "start": "node ./bin/www",
    "devstart": "nodemon ./bin/www",
    "serverstart": "DEBUG=super-cool-app:* npm run devstart"
  },
```

- Now, to run your applications, just run this in the command line.

```
npm run serverstart
```

---

### [Luxon](moment.github.io/luxon/#/)

- A helpful way to format time using JavaScript.

---

### [Mongoose](https://mongoosejs.com/docs/)

- Object modeling tool for MongoDB.

---

### [dotenv](https://www.npmjs.com/package/dotenv)

- Handles environment variables and secrets.

## [4] Middleware

Here's some useful middleware you can use in your Express projects.

### [Express Async Handler](https://www.npmjs.com/package/express-async-handler)

- Handles exceptions for async express routes.

---

### [Express Validator](https://www.npmjs.com/package/express-validator)

- Allows for sanitation and validation data.

---

### [Compression](https://www.npmjs.com/package/compression)

- Compresses the HTPP response sent to the client to reduce load times.

---

### [Helmet](https://www.npmjs.com/package/helmet)

- Protects against vulnerabilities by setting appropriate HTTP headers.

---

### [Express Rate Limit](https://www.npmjs.com/package/express-rate-limit)

- Limits repeated requests to public APIs and/or endpoints.

---

### [PassportJS](https://www.npmjs.com/package/passport)

- Handles authentication and sessions

---

### [bcryptjs](https://www.npmjs.com/package/bcrypt)

- Encryption for hashing passwords.
