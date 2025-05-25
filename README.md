# foodmate
Foodmate is a meal planning and recipe browsing web app that helps users discover recipes based on their preferences, dietary needs, and available ingredients. Built with Node.js, MongoDB, and Materialize CSS, it supports JWT authentication and third-party API integration.

# Running the Project with Docker
This branch focuses on how to dockerize foodmate. The following branch contains the `Dockerfile` and `docker-compose.yml`

A `Dockerfile` defines how to build a Docker image — a lightweight, standalone package that contains everything your app needs to run (code, dependencies, runtime, etc.).

`docker-compose.yml` defines and manages multi-container applications. It tells Docker how to run your containers (like your Node app and MongoDB) together.

## 1. How to Build the Image

From the root of your project (where the `Dockerfile` and `docker-compose.yml` live), run:

```
docker-compose build
```
## 2. How to Build the Image

From the root of your project (where the `Dockerfile` and `docker-compose.yml` live), run:

```
docker-compose up
```

## 3. Which Port to Access
The Node.js app listens on port 3000 inside the container. The container is mapped to the host machine's port 3000. To access the application open a browser and go to:

```
http://localhost:3000
```

## 4. What the /api/student Output Should Look Like
When you visit:
```
http://localhost:3000/api/student
```
You should get the following JSON response:

```json
{
    name: "Aprylle Joy Ablaza",
    studentId: 224698946
}
```