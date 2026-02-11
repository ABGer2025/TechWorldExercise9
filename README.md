# TechWorldExercise9

DevOps Bootcamp exercises for AWS services, CI/CD, and deployment.

## Exercises 1-9 Summary

1. Set up the Node.js app repository and baseline project structure.
2. Verified the app locally and ensured tests run.
3. Added containerization setup using Docker.
4. Configured a Jenkins pipeline using a shared library.
5. Built and pushed the Docker image from Jenkins.
6. Added docker-compose for deployment from configuration.
7. Added a deploy step to ship the image to an EC2 instance.
8. Opened EC2 security group port 3000 for browser access.
9. Added branch-based pipeline logic and GitHub webhook triggers.

## Current Setup

- Dockerfile: [app/Dockerfile](app/Dockerfile)
- Compose file: [app/docker-compose.yml](app/docker-compose.yml)
- Jenkins pipeline: [app/Jenkinsfile](app/Jenkinsfile)

## Notes

- Deploys run only on the `main` branch; other branches run tests only.
- EC2 host and deploy path are configured in the Jenkinsfile.
- Multibranch pipeline job: `node-app-mb` (main deploys, test runs tests only).
