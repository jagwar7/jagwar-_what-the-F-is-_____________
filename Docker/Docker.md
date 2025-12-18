====================================================================================================
What is Docker?
----------------

Docker is platform which package your applications which are under-development. This package called
Container. These  containers  can  run consistently  across  any  environment  (like your laptop, a
colleague's machine, a test server, or the cloud).
This containers ensures that we dont have to worry about specific systems or "Its works  fine on my
system"
---------------------------------------------------------------------------------------------------





====================================================================================================
What are the things Docker contains ?
------------------------------------

:=> 1. Your application code
:=> 2. Runtime (Node.js, Python, Java, etc.) 
:=> 3. System libraries (libc, openssl, etc.) 
:=> 4. Package manager (apt, apk, yum - depending on base image) 
:=> 5. Shell (bash, sh) 
:=> 6. Basic Unix tools (ls, cat, echo - if using full base image) 
:=> 7. Configuration files 
:=> 8. Environment variables
---------------------------------------------------------------------------------------------------






====================================================================================================
What is Docker Hub ?
--------------------


Docker Hub is a server, which contains so many environment of different type of  versions as well as
well as dependencies. Example: Node JS, Python, Java, Redis , Kafka and so many tools out there with
different verisons like: Node 24, Node 22, Node 18 and Python 3, Python 3.5 and so  many  other  web
tools like: Firebase, React, Axios and bluh bluh
---------------------------------------------------------------------------------------------------







====================================================================================================
What are the KEY-COMPONENTS of Docker ?
---------------------------------------

:=> 1. Dockerfile
    |    FROM node:18-alpine            <--------------The project will use Node v18 from Docker-Hub
    |    WORKDIR /app                   <-----Set the working directory inside the container to /app
    |    COPY package*.json ./  <-----Copy package.json from local to the container's /app directory
    |    RUN npm install                     <------ Install all dependencies listed in package.json
    |    COPY . .               <-----Copy everything else from your project folder to the container
    |    EXPOSE 5000                         <------Document that the container listens on port 5000
    |    CMD ["npm", "start"]              <--------Default command to run when the container starts


:=> 2. docker-compose.yml
    |    FROM node:18-alpine            <--------------The project will use Node v18 from Docker-Hub
    |    WORKDIR /app                   <-----Set the working directory inside the container to /app
    |    COPY package*.json ./  <-----Copy package.json from local to the container's /app directory
    |    RUN npm install                     <------ Install all dependencies listed in package.json
    |    COPY . .               <-----Copy everything else from your project folder to the container
    |    EXPOSE 5000                         <------Document that the container listens on port 5000
    |    CMD ["npm", "start"]              <--------Default command to run when the container starts
---------------------------------------------------------------------------------------------------


