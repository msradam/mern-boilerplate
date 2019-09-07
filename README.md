# 🍃 MERN Boilerplate
A dockerized boilerplate for full-stack web applications built with [M]ongoDB, [E]xpress, [R]eact, and [N]ode.

## Development with Docker
First, log-on to MongoDB Atlas and create a cluster. Make sure to whitelist the cluster to accept all incoming connections. Copy the connection string to the appropriate place in .env in the root directory.
Then, run:
```Bash
sudo docker-compose build
sudo docker-compose up
```

If all goes well, you should see the following output. 
```Bash
Starting mern-boilerplate_server_1 ... done
Starting mern-boilerplate_client_1 ... done
Attaching to mern-boilerplate_server_1, mern-boilerplate_client_1
server_1  | yarn run v1.17.3
server_1  | $ node index.js
client_1  | yarn run v1.17.3
server_1  | connecting to <your_mongodb_connection_string>
client_1  | $ react-scripts start
server_1  | Server running on port 8000
server_1  | connected to MongoDB
client_1  | Starting the development server...
client_1  | 
client_1  | Compiled successfully!
client_1  | 
client_1  | You can now view client in the browser.
client_1  | 
client_1  |   Local:            http://localhost:3000/
client_1  |   On Your Network:  http://172.18.0.3:3000/
client_1  | 
client_1  | Note that the development build is not optimized.
client_1  | To create a production build, use yarn build.
client_1  | 
```

The React app will be running on `http://localhost:3000` (or whatever port you specify in .env) and the Express app will be running on `http://localhost:8000` (or whatever port you specify in .env).

> Note: Do not use the same port for the client and server in .env. 

## Local developement without Docker
To develop locally without Docker, follow the above steps to setup MongoDB Atlas - however, change the .env file in the `server` directory. 
### Client Development
Run the following: 
```Bash
cd client 
yarn install
yarn start
```
The app will be running on `http://localhost:3000`.
### Server Development
Run the following:
```Bash
cd server
yarn install
yarn run dev
```
The app will be running on `http://localhost:8000` and will hot reload.


