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


### 4. Run DynamoDB Local Container.

I further integrated DynamoDB local into the existing [docker-compose file](https://github.com/Sanusi-bit/aws-bootcamp-cruddur-2023/blob/main/docker-compose.yml) to run the service as a container. Created a table named "Music" in the local volume of the DynamoDB and generated records from the table as shown in the image below.

![Image showing table generated from the DynamoDB local volume](https://github.com/Sanusi-bit/aws-bootcamp-cruddur-2023/blob/main/journal/assets/Dynamodb-table-week-1.png)


![Image showing table records generated from the DynamoDB local volume](https://github.com/Sanusi-bit/aws-bootcamp-cruddur-2023/blob/main/journal/assets/Dynamodb-table-records-week-1.png)

