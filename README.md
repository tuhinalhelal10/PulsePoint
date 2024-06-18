PulsePoint
Overview
Surveillance systems serve an important role in modern civilization, providing a core level of security, vast monitoring capabilities, and significant data collecting across several industries. However, technological advancements have shown shortcomings in classic closed-circuit surveillance settings. These systems struggle to manage growing data loads, lack adaptive access restrictions, and suffer integration issues with cutting-edge technology. PulsePoint, our technology, solves these limits via a distributed method, changing traditional closed-circuit technologies.

The PulsePoint system is a collection of services designed to manage cameras, users, video storage, and video analytics. It enables users to efficiently handle video feeds, perform analytics, and access a user-friendly frontend.

Research Paper
Revolutionizing Surveillance Technology with Distributed Systems
Services
Camera Management Service
Responsible for handling cameras, their registration, and stream URLs. Acts as an interface for camera data.

Dockerfile: Link to Dockerfile
User Management Service
Manages user authentication, registration, and login functionalities.

Dockerfile: Link to Dockerfile
Video Storage Service
Stores video files, manages uploads, and provides endpoints for fetching, deleting, and streaming videos.

Dockerfile: Link to Dockerfile
Video Analytics Service
Handles video analytics and processing tasks.

Dockerfile: Link to Dockerfile
Frontend
The user interface to interact with the entire system. It depends on all the other services.

Dockerfile: Link to Dockerfile
Setup
Requirements
Docker
Docker Compose
Installation
Clone this repository.
git clone https://github.com/abdullahwaseem01/PulsePoint.git
cd pulsepoint
Run Docker Compose to start the services.
docker-compose up
This will initialize all the services and databases required for the PulsePoint system.

Manual Startup (Alternative)
To start each service individually:

Navigate to the respective service directory.
cd camera-management-service
# OR
cd user-management-service
# OR
cd video-storage-service
# OR
cd video-analytics-service
# OR
cd frontend
Use the appropriate command to start each service, e.g.:
npm start
# OR
python app.py
# OR any command needed to start the service
Accessing Services
Camera Management Service: http://localhost:3002
User Management Service: http://localhost:3001
Video Storage Service: http://localhost:3003
Video Analytics Service: http://localhost:3004
Frontend: http://localhost:3000
Additional Details
MongoDB
The system uses MongoDB as its database. MongoDB is accessible on port 27017.

MongoDB Initialization Script: mongo-init.js
Docker Compose Configuration
The docker-compose.yml file includes service definitions, dependencies, and port mappings for each service in the system.
