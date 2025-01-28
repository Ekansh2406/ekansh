# Deployment Documentation


## Tasks
### Deploy Both Projects Using Docker Compose
1. **Dockerfiles**: Created Dockerfiles for both projects to define the environment and dependencies.
2. **docker-compose.yml**: Configured a `docker-compose.yml` file to manage the deployment of both projects.

### Network Configuration
- **TIP Project**: Mapped to port 3001 on localhost.
- **Nutrient-Tracker Project**: Mapped to port 3000 on localhost.

## Setup Process

### 1. Create Dockerfiles
Create Dockerfiles for both projects to define the environment and dependencies.

### 2. Configure docker-compose.yml
Configure the `docker-compose.yml` file to define services, networks, and volumes.

### 3. Running Containers
Verify running containers using `docker ps`.

### 4. Accessing Websites
Access the TIP project successfully on port 3001.

### Issues Encountered
- **Nutrient-Tracker Project**: Encountered issues with deploying the Nutrient-Tracker project. Despite configuring the Dockerfile and `docker-compose.yml`, the project did not run successfully on the chosen port.

### Screenshots
- **Running Containers**: Provided a screenshot of the running containers using `docker ps`.
- **Accessing TIP Project**: Provided a screenshot of accessing the TIP project in the browser.

## Conclusion
While the TIP project was successfully deployed and accessible on port 3001, the Nutrient-Tracker project encountered deployment issues. Further troubleshooting is required to resolve the issues with the Nutrient-Tracker project.