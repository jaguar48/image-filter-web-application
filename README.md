# Udagram Image Filtering Application

This is an image filter microservice application that uses Kubernetes and Travis CI for scalable deployment.. The initial challenge was setting up an automatic deployment pipeline which was made possible with Travis CI. The CI built the image and pushed it to DockerHub. I also had to write Kubernetes manifest files for the microservice where I did load balancing, Scaling, Self healings on the pods. Deployment was also triggered by Travis CI.
You can find the attached screenshots on the project folders.


The project is split into two parts:

1. Frontend - Angular web application built with Ionic Framework
2. Backend RESTful API - Node-Express application

## Getting Started

> _tip_: it's recommended that you start with getting the backend API running since the frontend web application depends on the API.

### Prerequisite

1. The depends on the Node Package Manager (NPM). You will need to download and install Node from [https://nodejs.com/en/download](https://nodejs.org/en/download/). This will allow you to be able to run `npm` commands.
2. Environment variables will need to be set. These environment variables include database connection details that should not be hard-coded into the application code.
