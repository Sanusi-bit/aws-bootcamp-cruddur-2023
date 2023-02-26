# Week 1 — App Containerization

## Required Homework/Tasks

### 1a. Containerizing frontend and backend applications individually.

I created the dockerfile for both the frontend and backend of the application and successfully ran the container for both individually. Here is the link to the [Frontend](https://github.com/Sanusi-bit/aws-bootcamp-cruddur-2023/blob/main/frontend-react-js/Dockerfile) and [backend](https://github.com/Sanusi-bit/aws-bootcamp-cruddur-2023/blob/main/backend-flask/Dockerfile) Dockerfiles.

![Image for Frontend container of the application](https://github.com/Sanusi-bit/aws-bootcamp-cruddur-2023/blob/main/journal/assets/Frontend-Containerization-week-1.png)

![Image for backend container of the application](https://github.com/Sanusi-bit/aws-bootcamp-cruddur-2023/blob/main/journal/assets/Backend-containerization-week-1.png)


### 1b. Containerizing frontend and backend applications simultaneously using Docker compose.

I created a docker-compose file to build the images for both frontend and backend and run the containers simultaneously. Here is the [link](https://github.com/Sanusi-bit/aws-bootcamp-cruddur-2023/blob/main/docker-compose.yml) to the Docker-compose file and the image showing all ports served accurately for the application to be deployed.

![Image of all ports served on both frontend and backend of the application to verify successful running of both containers](https://github.com/Sanusi-bit/aws-bootcamp-cruddur-2023/blob/main/journal/assets/docker-compose-week-1.png)

![Cruddur home page verifying successful running of frontend and backend containers](https://github.com/Sanusi-bit/aws-bootcamp-cruddur-2023/blob/main/journal/assets/Cruddur-home-week-1.png)


### 2. Creating a notification endpoint 

I created the API Endpoints for the notification feature in the [OpenAPI](https://github.com/Sanusi-bit/aws-bootcamp-cruddur-2023/blob/main/backend-flask/openapi-3.0.yml) file then created notification activities [module](https://github.com/Sanusi-bit/aws-bootcamp-cruddur-2023/blob/main/backend-flask/services/notifications_activities.py) as a service to be used in the overall app. 

![Image for notifications endpoint](https://github.com/Sanusi-bit/aws-bootcamp-cruddur-2023/blob/main/journal/assets/Notifications-api-endpoint-week-1.png)


### 3. Implemented the notifications page using react

Created the frontend page for the notifications feed feature of the cruddur app using react and used React router to route it to the app. Here is the [link](https://github.com/Sanusi-bit/aws-bootcamp-cruddur-2023/blob/main/frontend-react-js/src/pages/NotificationsFeedPage.js) to the Notifications Feed page with a post from User(Sanusi Waris) saying (I am beautiful) being notified

![Image of the Notifications page](https://github.com/Sanusi-bit/aws-bootcamp-cruddur-2023/blob/main/journal/assets/Notifications-FeedPagwe-week-1.png)


### 4. Running DynamoDB Local Container.

I further integrated DynamoDB local into the existing [docker-compose file](https://github.com/Sanusi-bit/aws-bootcamp-cruddur-2023/blob/main/docker-compose.yml) to run the service as a container. Created a table named "Music" in the local volume of the DynamoDB and generated records from the table as shown in the image below.

![Image showing table generated from the DynamoDB local volume](https://github.com/Sanusi-bit/aws-bootcamp-cruddur-2023/blob/main/journal/assets/Dynamodb-table-week-1.png)


![Image showing table records generated from the DynamoDB local volume](https://github.com/Sanusi-bit/aws-bootcamp-cruddur-2023/blob/main/journal/assets/Dynamodb-table-records-week-1.png)

### 5. Running Postgres Container.
I installed postgres client into Gitpod using the code below. I then connected successfully to the postgresql using the Database explorer on gitpod and the gitpod codespace.  

```yml

- name: postgres
    init: |
      curl -fsSL https://www.postgresql.org/media/keys/ACCC4CF8.asc|sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/postgresql.gpg
      echo "deb http://apt.postgresql.org/pub/repos/apt/ `lsb_release -cs`-pgdg main" |sudo tee  /etc/apt/sources.list.d/pgdg.list
      sudo apt update
      sudo apt install -y postgresql-client-13 libpq-dev

```

I further integrated Postgres local into the existing [docker-compose file](https://github.com/Sanusi-bit/aws-bootcamp-cruddur-2023/blob/main/docker-compose.yml) to run the service as a container.

![Postgresql Database explorer succesful connection](https://github.com/Sanusi-bit/aws-bootcamp-cruddur-2023/blob/main/journal/assets/postgresql-db-explorer-week-1.png)

![Postgre client successful connection after running the container](https://github.com/Sanusi-bit/aws-bootcamp-cruddur-2023/blob/main/journal/assets/postgresql-client-week-1.png)


## Homework Challenges

### 1. Tag and push an image to dockerhub.

I started this challenge by building a simple image, tagged the image and pushed the image to dockerhub. The instructions are seen below.

- Create an account on [Docker Hub](https://hub.docker.com/) and take note of your username.
- Let's build a simple python image with the following libraries (numpy 1.14.3, matplotlib 2.2.2, seaborn 0.8.1)
- Ensure docker is installed on your local PC or instance. You can follow this [link](https://docs.docker.com/desktop/install/) to install docker based on your OS.
- Create a folder called 'Challenges'
```
mkdir Challenges
```
- Change into the 'Challenges' folder created
```
cd Challenges
```
- Create a dockerfile
```
touch Dockerfile
```
- Paste the code below into the Dockerfile
```
FROM python:3.8-buster
RUN pip install --upgrade pip
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY src/ .
CMD [ "python", "aws-bootcamp.py"]
```
- Create a requirements.txt file
```
touch requirements.txt
```
- Paste the code below for the required libraries into the requirements file
```
numpy==1.14.3
matplotlib==2.2.2
seaborn==0.8.1
```
- Create a sub-folder in the Challenges folder named "src"
```
mkdir src
```
- Login to your Dockerhub account using the code below. Once prompted for username, input the username for your dockerhub account to log you in successfully.
```
docker login -u Username
```
- Build the docker image from the docker file created with a tag "aws-bootcamp".
```
docker build -t aws-bootcamp ./Challenges/Dockerfile
```
- Tag the docker image built
```
docker image tag aws-bootcamp Username/aws-bootcamp:latest
```
- Push the image to docker hub
```
docker image push Username/aws-bootcamp:latest
```
Login to your dockerhub account to see your image under repositories.
![Image pushed to Docker Hub](https://github.com/Sanusi-bit/aws-bootcamp-cruddur-2023/blob/main/journal/assets/dockerhub-image-week-1.png) 

