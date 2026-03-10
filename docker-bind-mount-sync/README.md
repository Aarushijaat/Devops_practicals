"#Docker Bind Mount Sync Practical"

\# Practical: Docker Bind Mount Sync



\## Objective



To understand how Docker \*\*bind mounts\*\* work and how files can be synchronized between the \*\*host system and a Docker container\*\*.



\## Introduction



A \*\*bind mount\*\* allows a directory or file from the host machine to be mounted inside a Docker container.

This enables real-time synchronization between the host and the container.



Any changes made in the host directory will immediately reflect inside the container.



Bind mounts are commonly used in:



\* Development environments

\* Sharing configuration files

\* Syncing application source code



\## Prerequisites



\* Docker installed on the system

\* Basic knowledge of Docker commands

\* A running Docker daemon



\## Steps



\### 1. Create a directory on the host



```bash

mkdir webdata

cd webdata

```



\### 2. Create a sample file



```bash

echo "Hello from Host Machine" > index.html

```



\### 3. Run a Docker container with bind mount



```bash

docker run -d -p 8080:80 -v ${PWD}:/usr/share/nginx/html nginx

```



Explanation:



\* `-d` → Run container in detached mode

\* `-p 8080:80` → Map host port 8080 to container port 80

\* `-v ${PWD}:/usr/share/nginx/html` → Mount current host directory inside container



\### 4. Access the application



Open a browser and go to:



```

http://localhost:8080

```



You should see the content of \*\*index.html\*\*.



\### 5. Test synchronization



Modify the file on the host:



```bash

echo "File Updated Successfully" > index.html

```



Refresh the browser and the changes will appear immediately.



\## Expected Output



The web page served by the container updates automatically whenever the host file changes.



\## Conclusion



This practical demonstrates how \*\*Docker bind mounts allow real-time file synchronization between the host and container\*\*, which is useful for development and debugging workflows.



