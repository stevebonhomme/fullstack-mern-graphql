# Full Stack Mern Application Using GraphQL

This repository is for a proof of concept I built using React and is powered by MongoDB Atlas, Apollo Client, GraphQL, and Express Framework.  This is a project management application that allows the addition of users as well as projects with the ability to set project status as started, in progress or completed.

![Project Management App Frontend](projectManagementApp.jpg "Project Management App")

## Why These Technologies?

Before going further, let's talk about the technologies we'll use for the application stack.

#### MongoDB Atlas 
The most advanced cloud database service on the market for MongoDB, with unmatched data distribution and mobility across AWS, Azure, and Google Cloud, built-in automation for resource and workload optimization, and so much more.

#### React and Apollo Client

React is one of the most popular JavaScript frameworks with a great community. It's also versatile, allowing you to build both web and mobile applications.

Apollo Client is a fully-featured GraphQL client that allows you to build user interface components and fetch data via GraphQL seamlessly. The Apollo Client is also one of the most popular GraphQL clients.

Together, React and Apollo Client form a powerful combination that fits the requirements for the real-time voting application.

#### Express Framework

Express.js, or simply Express, is a back end web application framework for Node.js, released as free and open-source software under the MIT License. It is designed for building web applications and APIs. It has been called the de facto standard server framework for Node.js.

#### Bootstrap

Bootstrap is a free and open-source CSS framework directed at responsive, mobile-first front-end web development. It contains HTML, CSS and JavaScript-based design templates for typography, forms, buttons, navigation, and other interface components. Bootstrap makes it easy to style any project.

## GraphQL Queries & Mutations

GraphQL is an open spec for a flexible API layer. Put GraphQL over your existing backends to build products faster than ever before. 

## Get names of all clients
```
{
  clients {
    name
  }
}
```

## Get a single client name and email
```
{
  client(id: 1) {
    name
    email
  }
}
```

## Get name and status of all projects
```
{
  projects {
    name
    status
  }
}
```

## Get a single project name, description along with the client name and email
```
{
  project(id: 1) {
    name
    description,
    client {
      name
      email
    }
  }
}
```

## Create a new client and return all data
```
mutation {
  addClient(name: "Tony Stark", email: "ironman@gmail.com", phone: "955-365-3376") {
    id
    name
    email
    phone
  }
}
```

## Delete a client and return id
```
mutation {
  deleteClient(id: 1) {
    id
  }
}
```

## Create a new project and return name and description
```
mutation {
  addProject(name: "Mobile App", description: "This is the project description", status: "new", clientId: "1") {
   name
   description
  }
}
```

## Update a project status and return name and status
```
mutation {
  updateProject(status: "completed") {
   name
   status
  }
}
```

## Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)

 
