# Unit 3 Practicals

Contains the practicles carried out in Unit 3 of Docker and Docker Compose.
Practicles includes creation of containers, deployment of multiple container application and conversion of docker run command to Docker Compose.

## Folder Structure

unit-3-practicals/
├── README.md
├── wordpress-compose/
├── node-mongo-compose/
└── wordpress-run-to-compose/

Exercise 1: Node.js + MongoDB using Docker Compose

This is a hands-on project in which a Node.js application is linked to MongoDB using Docker Compose along with a Dockerfile that is built for the Node.js application.

Files Used:
- server.js
- package.json
- Dockerfile
- docker-compose.yml

Execution Command:
- docker compose up --build -d

Expected Output: 
- On your web browser, it will show "Node.js + MongoDB running with Docker Compose."

Visit: http://localhost:3001

Exercise 2: WordPress with MySQL Using Docker Compose

This exercise provides a demonstration on deploying a WordPress application along with a MySQL database using Docker Compose. There are two services used in the configuration – one for WordPress and another for MySQL.

Files needed:
- docker-compose.yml

Command to execute:
- docker compose up -d

Expected output:
Your WordPress site should now be accessible from your browser by visiting:
http://localhost:8082

Exercise 3 : Convert Docker run command into Docker Compose
In this practical experiment, the Dockerfile and the docker run command were replaced by the Docker Compose configuration.

Files Utilized
- docker-compose.yml

Command Executed
- docker compose up -d

Output
- You will be able to access the WordPress website via the web browser at http://localhost:8083

Topics Explored
- Docker Images
- Containers
- Dockerfile
- Docker Compose
- Port Forwarding
- Environment Variables
- Volume Mounts
- Multi-container Applications

Conclusion
- This practice exercise shows the use of Docker Compose for developing multi-container applications.
