# Deployment Documentation

## Overview
This document outlines the steps taken to deploy two projects, Nutrient-Tracker and TIP, using Docker containers on localhost. The Nutrient-Tracker project is a Ruby on Rails application, while the TIP project is a Next.js application. Both projects were configured and deployed using Docker Compose.

## Repositories
- **Nutrient-Tracker**: A Ruby on Rails project.
- **TIP**: A Next.js project.

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

#### Nutrient-Tracker Dockerfile
```Dockerfile
# Use the official Ruby image as a parent image
FROM ruby:2.7

# Set the working directory
WORKDIR /app

# Copy the Gemfile and Gemfile.lock into the image
COPY Gemfile* ./

# Install dependencies
RUN bundle install

# Copy the rest of the application code
COPY . .

# Expose port 3000 to the outside world
EXPOSE 3000

# Start the Rails server
CMD ["rails", "server", "-b", "0.0.0.0"]
```

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

## Attachments
- Dockerfiles for both projects.
- `docker-compose.yml` script.
- Screenshots of running containers and accessing the TIP project.