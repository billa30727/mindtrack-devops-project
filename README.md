# MindTrack DevOps Project

## Project Overview

MindTrack is a React-based task management application deployed using a complete DevOps pipeline on AWS.

This project demonstrates:

- React Application Deployment
- Docker Containerization
- Kubernetes Orchestration using AWS EKS
- CI/CD Automation using AWS CodeBuild and CodePipeline
- Monitoring using AWS CloudWatch
- GitHub Integration

The application runs on Port 3000 and is deployed using Kubernetes LoadBalancer service.

---

# Architecture Diagram

```text
                    +------------------+
                    |   GitHub Repo    |
                    +------------------+
                              |
                              v
                    +------------------+
                    | AWS CodePipeline |
                    +------------------+
                              |
                              v
                    +------------------+
                    | AWS CodeBuild    |
                    +------------------+
                              |
                              v
                    +------------------+
                    | Docker Image     |
                    +------------------+
                              |
                              v
                    +------------------+
                    | DockerHub / ECR  |
                    +------------------+
                              |
                              v
                    +------------------+
                    | AWS EKS Cluster  |
                    +------------------+
                              |
                              v
                    +------------------+
                    | Kubernetes Pods  |
                    +------------------+
                              |
                              v
                    +------------------+
                    | LoadBalancer     |
                    +------------------+
                              |
                              v
                    +------------------+
                    | React Application|
                    +------------------+
