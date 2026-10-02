\# Node.js CI/CD Demo App



\## Overview



This project demonstrates an automated CI/CD pipeline using GitHub Actions, Node.js, Docker, and Docker Hub.



Whenever code is pushed to the `main` branch, GitHub Actions automatically runs tests, builds a Docker image, and pushes the image to Docker Hub.



\## Technologies Used



\- Node.js

\- Express.js

\- Jest

\- Docker

\- Docker Hub

\- GitHub

\- GitHub Actions



\## Application



The application is a simple Node.js web application built using Express.js.



It runs on port `3000`.



\## CI/CD Pipeline



The GitHub Actions workflow performs the following steps:



1\. Checkout the source code.

2\. Set up Node.js.

3\. Install dependencies using `npm ci`.

4\. Run automated tests using `npm test`.

5\. Log in to Docker Hub using GitHub Secrets.

6\. Build the Docker image.

7\. Push the Docker image to Docker Hub.



\## Pipeline Flow



```text

GitHub Push

&#x20;    ↓

Run Tests

&#x20;    ↓

Build Docker Image

&#x20;    ↓

Push to Docker Hub

