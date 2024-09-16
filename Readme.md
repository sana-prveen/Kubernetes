# Hello World App - Kubernetes Deployment

This project demonstrates how to create a simple web application, containerize it using Docker, deploy it to a Kubernetes cluster, and expose it externally using a Kubernetes LoadBalancer Service.

## Prerequisites

Before setting up and running this project, ensure you have the following installed on your machine:

- [Docker]
- [Minikube]
- [Kubectl]
- [Git]

## Setup Instructions

### Step 1: Clone the repository

Clone the project repository to your local machine:
git clone https://github.com/yourusername/your-repository.git
cd your-repository

### Step 2: Use Docker to build the image for the web application:

docker build -t hello-world-app:latest .

### Step 3:If you haven't already started Minikube, run the following:

minikube start

### Step 4: Deploy to Kubernetes:

kubectl apply -f deployment.yaml

### Expose the application with a service:

kubectl apply -f service.yaml

### Verify the deployment and service:

kubectl get pods
kubectl get services

### Step 5:Access the Application:

minikube tunnel

### To stop minikube:

minikube stop

### to start service in kubernetes:

minikube service hello-world-app
