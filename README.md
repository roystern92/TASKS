## Tasks
A Tasks management software for daily tasks. 

## Status
This project is over and has been deployed.

[![Image from Gyazo](https://i.gyazo.com/8af73e1ee6214d7559ff057c22440a87.png)](https://gyazo.com/8af73e1ee6214d7559ff057c22440a87)

[![Image from Gyazo](https://i.gyazo.com/485d11fbe4fd65c23b196ef6c56908f9.gif)](https://gyazo.com/485d11fbe4fd65c23b196ef6c56908f9)
 
[![Image from Gyazo](https://i.gyazo.com/ce9152d04e390fe65fc15caab6375169.gif)](https://gyazo.com/ce9152d04e390fe65fc15caab6375169)
 
[![Image from Gyazo](https://i.gyazo.com/95e81294c14f69a7914f822518a35788.gif)](https://gyazo.com/95e81294c14f69a7914f822518a35788)
 
[![Image from Gyazo](https://i.gyazo.com/bac0b33e20d64cf645b0175fece9445c.gif)](https://gyazo.com/bac0b33e20d64cf645b0175fece9445c)
 
## Installation and Setup Instructions

#### Prerequisites
`node` & `npm` must be installed globally on your machine.


`Mongo Atlas Account` must create a mongo atlas cluster and connect it to the app. Just create an account and add your connection string into mongoAtlasUri variable in app.js file.

[![Image from Gyazo](https://i.gyazo.com/aa6d7ac9de76551cf2325d04805b576b.gif)](https://gyazo.com/aa6d7ac9de76551cf2325d04805b576b)

[![Image from Gyazo](https://i.gyazo.com/cfa88eae77dc0f17c55d1481ea99b60f.png)](https://gyazo.com/cfa88eae77dc0f17c55d1481ea99b60f)

make sure to set the Network access to your IP or to 0.0.0.0/0 so anyone can connect to it.

[![Image from Gyazo](https://i.gyazo.com/ea6e6341f2dd488b4f3886bfc14842e4.png)](https://gyazo.com/ea6e6341f2dd488b4f3886bfc14842e4)


#### Installation:

Clone down this repository. 

Navigate to client and server folder and run:  

`npm install`  

You will need to run the client and the server separately.  
Navigate to the client and the server folders from different terminal windows and run:

`npm start`  

To Visit the App client:

`localhost:3000/`  

The server run locally on:

`localhost:8080/`  

## Reflection

This was a 1 month long project built after studying for a while javascript, node.js and react. Project goals included using technologies learned up until this point and build my first edge to edge project.
  
Originally I wanted build an application that allowed users to create a todo list for the current day and manage it. 

I started the process by building the server as a rest api. I used `express.js` to create the web server and `mongoose` to model the application data. I created 3 different mongoose schemas to control the application data: User, List, TodoItem.
I divided the endpoints of the api to different files. `Admin` endpoints that handle with request from an authenticated user to mange his todo list and `Auth` endpoints for an unauthenticated user that want to create an new account or login to an active one.
Each file, Admin and Auth has a matching file with the same name, in the controller folder, with all the middlewares that handle their endpoints.

After testing the the web server with postman and make sure the data is well saved in MongoDB Atlas I start working on the client side of the app. I started this process by using  the `create-react-app` boilerplate, then adding `react-router`. I used `redux` in order to centralized the application state and `redux-thunk` for handling asynchronous services from the redux store. I used `axios` for handling requests from the client to the server. I created most of the UI component that are used in this project and styled them so i can reuse them in a future projects.    

One of the main challenges I ran into was when i was editing the tasks. After editing a task, it make a PUT request to the server to update the task. so it takes time to render the change in the notebook board. This lead me to spend a few days on a research how to render the changes much more faster. One more challenge I ran into was Authentication. This lead me on a research spike into jwt (JsonWebToken), method for representing claims securely between two parties.

At the end of the day, the technologies implemented in this project are React, React-Router, Redux, Bootstrap, ReactStrap, ReactScroll, ReactContextMenu, Node.js, Express.js, Mongoose, ExpressValidator, Bcryptjs, Cors, Multer, Jsonwebtoken and a significant amount of CSS. I chose to use the `create-react-app` boilerplate to minimize initial setup and invest more time in diving into weird technological rabbit holes.