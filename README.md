Detailed documentation
1.	Overview:
This project explains how to launch a microservice on Google Cloud Platform (GCP) using Docker and Artifact Registry. The microservice is constructed using Node.js and deployed in a containerized environment.

2.	Prerequisites
•	Install and configure Google Cloud SDK in the system
•	Install and configure Docker in the system
•	Install Google Cloud Platform Project with billing enabled

####
4.	Setting up and Configuration
#####
•	Use the command gcloud init to initialize the Google cloud CLI
•	gcloud auth configure-docker australia-southeast1-docker.pkg.dev command is used to configure the authentication of docker for Google Artifact Registry
•	Next, we need to clone the repository using git clone <repository_name>. Here, the repository name is SIT737-2025-prac5p. Navigate to the repository using the command cd SIT737-2025-prac5p.
•	To build the docker image, we use the command docker build -t myapp .
•	‘docker tag myapp australia-southeast1-docker.pkg.dev/sit737-25t1-anand-b26c383/sit737ishi/myapp:latest’  command is used for tagging the image to google artifact registry.
•	‘docker push australia-southeast1-docker.pkg.dev/sit737-25t1-anand-b26c383/sit737ishi/myapp:latest’  command is used for pushing the image to google artifact registry.
•	‘docker run -d -p 8081:3000 gcr.io/sit737-25t1- anand-b26c383/myapp:latest’ command is used to check that it can boot the microservice from published container.	
