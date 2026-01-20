# DevOps Assignment – Cloud Run Deployment

## Overview
This repository contains a simple HTTP application and its complete DevOps implementation using Google Cloud Platform (GCP). The project demonstrates source code management, containerization, cloud networking, and automated deployment using a serverless approach.

The application is containerized using Docker and deployed to Google Cloud Run. A custom VPC, subnet, and Serverless VPC Access Connector are configured to enable secure network communication.


## Repository Structure

├── app/
│ ├── init.py
│ └── main.py
├── Dockerfile
├── requirements.txt
├── .github/
│ └── workflows/
│ └── devops-app-pipeline.yml
└── README.md

## Application Details
- Simple HTTP backend application
- Exposes `/health` endpoint
- `/health` endpoint returns service status
- Configurable port via container runtime

## CI/CD Pipeline
- Implemented using **GitHub Actions**
- Triggers on push to `dev` and `main` branches
- Builds Docker image
- Pushes image to **GCP Artifact Registry**
- Automatically deploys to **Google Cloud Run**


## Cloud Infrastructure:-
    
## VPC and Subnet
- Custom VPC created for network isolation
- Subnet configured within the VPC for controlled IP allocation

### Serverless VPC Access Connector
- Configured to allow Cloud Run to access resources inside the VPC
- Enables secure communication with private network resources

### Cloud Run Deployment
- Deployed as a serverless containerized service
- Publicly accessible via HTTPS
- Built-in load balancing and auto-scaling provided by GCP

