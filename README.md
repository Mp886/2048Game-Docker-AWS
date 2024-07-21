# 2048Game-Docker-AWS

This project involves creating a Dockerized version of the 2048 game and deploying it to AWS Elastic Beanstalk.

Features
- Clone the 2048 game from GitHub
- Create a Docker image for the game
- Deploy the Docker image to AWS Elastic Beanstalk

Prerequisites
- Docker
- AWS CLI
- AWS Elastic Beanstalk CLI
- Git

#Clone the Repository

git clone https://github.com/gabrielecirulli/2048.git
cd 2048

# Dockerization
 # Create a Dockerfile
You can use the Dockerfile provided in the repository or else you can create your u=own dockerfile with correct Instructions and arguments.

 # Build the Docker Image
Build the docker image From the dockerfile you have to create a docker image by using command "docker build" with the required parameters. For the entire command, i have given the command below. In the below command "-t" specifies the name of the image. In my case i have given 2048game for my image. You can use the same tag name or your desired tag name.

docker build -t 2048game .

# Run the Docker Container



  
