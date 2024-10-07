# Simple Kubernetes App

## Description

This repository contains a simple Kubernetes application demonstrating a microservices-based architecture. It includes a voting app, result app, Postgres database, Redis cache, and a worker component, all deployed using Kubernetes Deployments and Services.

### Features

- **Voting App**: Allows users to submit their votes.
- **Result App**: Displays the results of the voting process, retrieving data from the Postgres database.
- **Postgres Database**: Manages persistent storage for the voting results.
- **Redis Cache**: Provides in-memory caching to enhance performance and reduce latency for frequent data retrieval.
- **Worker Component**: Processes background tasks to ensure smooth operation of the application.

This app showcases the use of multiple containerized services working together within a Kubernetes cluster, highlighting the benefits of using Redis for caching and Postgres for reliable data storage.

## Prerequisites

Before deploying the application, ensure you have the following installed:

- **Docker**: Required to run the container images.
- **Kubectl**: Command-line tool for interacting with Kubernetes clusters.
- **Minikube**: Creates a local Kubernetes cluster on your machine.

## Deployment Instructions

Follow these steps to deploy the application:

1. **Start Minikube**  
   Launch your local Kubernetes cluster with the following command:<br>
   `minikube start`

2. **Clone the Repository**  
   Clone this repository to your local machine:<br>
   `git clone https://github.com/Dhia-BH/simple_kuberentes_app.git`<br>
   `cd simple_kuberentes_app`

3. **Deploy the Application**  
   Create the Kubernetes resources using the YAML files provided in the repository:<br>
   `kubectl apply -f voting-app-deploy.yaml`<br>
   `kubectl apply -f postgres-deployment.yaml`<br>
   `kubectl apply -f redis-deployment.yaml`<br>
   `kubectl apply -f result-app-deployment.yaml`<br>
   `kubectl apply -f worker-app-deployment.yaml`<br>

5. **Access the Voting Interface**  
   To access the voting interface, use the following command to get the Minikube service URL:<br>
   `minikube service voting-app-deployment --url`<br>
   This will return the URL where you can access the voting application.

6. **Check Deployment Status**  
   You can check the status of your deployments and pods with:<br>
   `kubectl get deployments`<br>
   `kubectl get pods`

7. **Stop Minikube**  
   When you are done testing, you can stop Minikube with:<br>
   `minikube stop`

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
