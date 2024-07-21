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
Run the Docker Container After creating the image, now you need to run the container by using "docker run" command, which helps you to create a container and run your image in the container. For the entire command, i have given the command below. Here in the below command you can see "-P' wich is port mapping, so this app will run only in the port 80. I have also given this port mapping in the docker file too.

docker run -it -d -p 80:80 2048game

-Open your browser and go to http://localhost:80 to see the game running in the Docker container.

# Deploy to AWS Elastic Beanstalk

1) Log in to AWS Management Console:

- Go to AWS Management Console.

2) Navigate to Elastic Beanstalk:
- In the AWS Management Console, search for "Elastic Beanstalk" in the search bar and select it.

3) Create a New Application:

- Click on "Create a new application."
- Enter an application name (e.g., 2048 Game).
- Click "Create."

4) Create an Environment:

- Click on "Create a new environment."
- Select "Web server environment."
- Click "Select."

5) Configure Environment:

- Enter an environment name (e.g., 2048-game-env).
- For "Platform," select "Docker."
- For "Platform Branch," select "Docker running on 64bit Amazon Linux 2."

6) Upload Dockerfile:

- In the "Source" section, choose "Upload your code."
- Upload the Dockerfile.

7) Review and Create Environment:

- Review your settings.
- Click "Create environment."

AWS Elastic Beanstalk will create the environment and deploy the Docker container. Once the environment is created, you will see a URL to access your application.

8) Access Your Application:

- Open your browser and navigate to the provided URL to see the 2048 game running.


  
