# Quick-start-with-docker
## Installation Guide
```
1. sudo snap install docker
2. install Docker Desktop 
```
## Setup docker for FrontEnd
#### Dockerfile
```
FROM node
WORKDIR /app
COPY ./package*.json ./
RUN npm install
EXPOSE 3000
COPY . .
# Define the command to run the application
CMD [ "npm", "start" ]
```
#### .dockerignore
```
node_modules
npm-debug.log
```
---
# Docker Used for 
- [x] consistent environment
- [x] fast and light weight
- [x] isolated and secure 

# Imp CMD
1. create docker Image ------>     docker build -t [imageName]
2. run docker Image--------->      docker run -d -p 3000:3000 -v $(pwd):/app [imageName]
3. run in interactive mode -->     docker exec -it [CID] or [CN] bash
  
![Screenshot from 2023-05-19 08-51-20](https://github.com/webdev-ashishk/Quick-start-with-docker/assets/127021921/4493ece3-b457-4c30-81f5-4455fe40aab2)
