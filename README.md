# Kotlin Application Dockerization

This README provides instructions on how to build a Docker image for a Kotlin application, run it, and execute CURL commands to interact with the application.

## Prerequisites

- Docker installed on your machine
- Kotlin project setup with Gradle

## Steps

### 1. Build the `Dockerfile`

Run the command:

`docker build -t test-kotlin-app .`

### 2. Run the Docker Container
`docker run -p 8080:8080 test-kotlin-app`

### 3. Execute CURL Commands to Create a message
```sh
curl -X POST http://localhost:8080/ \
     -H "Content-Type: application/json" \
     -d '{"text": "Test1!"}'
```

### 4. Execute CURL Commands to Retrieve all messages
```sh
curl -X GET http://localhost:8080/
```
