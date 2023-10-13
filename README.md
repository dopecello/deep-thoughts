# Deep Thoughts

This is a project that I worked on that is one of my first full-stack MERN applications. This also uses GraphQL to act as a sort of API between the user and the MongoDB database.

## Local Setup

There are three areas of dependencies: the root directory, `/client` and `/server`. Make sure to follow the instructions carefully.
- `cd` into the root f the application and install dependencies using `npm i`
- After that is completed, run `npm run install`. This will leverage the `concurrently` package and install dependencies in both `/client` and `/server`

**For Live Development**

All you need to do, after all dependencies are install is run `npm run develop` in the root directory. This will start the Express and Apollo servers and will also initiate the frontend development environment.

**Seeding the Database**

While not strictly necessary, I have provided some mock data if you would like to test interactions between different mock users and their posts. This is good if you are refactoring.

**Service Worker**

There is the option of implementing a service worker in this project. Navigate to `./client/src/index.js` to view the implementation of the service worker. You can comment out `serviceWorker.register()` if you don't wish to use it. However, service workers are beneficial because they let the app load faster on subsequent visits in production, and gives it offline capabilities. However, it also means that developers (and users) will only see deployed updates on subsequent visits to a page, after all the existing tabs open on the page have been closed, since previously cached resources are updated in the background.
