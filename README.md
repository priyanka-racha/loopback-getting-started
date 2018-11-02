### Steps for cloning GitHub repository:

1. Create a directory - `mkdir git_repo`
2. Move to git repository folder - `cd git_repo`
3. Clone git repository - `git clone https://github.com/strongloop/loopback-getting-started.git` 
4. List files -`ls-ltr` 
5. Move to git project repository folder - `cd loopback-getting-started`
6. List files -`ls-ltr`
7. Check git status -`git status`

### Dockerizing the cloned application:

8. Create a Dockerfile with below content - `vi Dockerfile`
   ```
    FROM node:slim
    ADD . /app
    WORKDIR /app
    EXPOSE 3000
    RUN npm install
    RUN npm start
    ```
9. List docker images - `docker images`
10. Build docker image -`docker build -t coffeeshop-api-img`
11. List docker images - `docker images`
12. Create docker container for project - `docker run -d -p 3000:3000 --name coffeeshop-api-cont coffeshop-api-img`
13. List docker containers -`docker container ls`
14. Open URL in browser - http://localhost:3000/explorer
