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
