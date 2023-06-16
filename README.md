# DockerServerClient
1. What is a docker container? 
A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries and settings.

2. What is the difference between a container and a virtual machine? 
Containers and virtual machines have similar resource isolation and allocation benefits, but function differently because containers virtualize the operating system instead of hardware. Containers are more portable and efficient.

Containers are an abstraction at the app layer that packages code and dependencies together. Multiple containers can run on the same machine and share the OS kernel with other containers, each running as isolated processes in user space.

Virtual machines (VMs) are an abstraction of physical hardware turning one server into many servers. The hypervisor allows multiple VMs to run on a single machine.  

3. What is the purpose of a Dockerfile? 
A Dockerfile is a text document that contains all the commands a user could call on the command line to assemble an image. Using docker build users can create an automated build that executes several command-line instructions in succession so that the user doesn't have to.

4. What is the purpose of a requirements.txt file? 
The requirements.txt file is a list of dependencies that are called in the Dockerfile with pip3 install to ensure that when the user runs the docker image they have the same working environment.

5. What is the purpose of a docker-compose.yml file? 
Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a YAML file to configure your application’s services. Then, with a single command, you create and start all the services from your configuration. To learn more about all the features of Compose, see the list of features. Run your Docker app with 'docker-compose up' 

6. What is the difference between a docker image and docker container? 
A Docker image is an immutable (unchangeable) file that contains the source code, libraries, dependencies, tools, and other files needed for an application to run.

Since images are, in a way, just templates, you cannot start or run them. What you can do is use that template as a base to build a container. A container is, ultimately, just a running image. Once you create a container, it adds a writable layer on top of the immutable image, meaning you can now modify it.

The image-base on which you create a container exists separately and cannot be altered. When you run a containerized environment, you essentially create a read-write copy of that filesystem (docker image) inside the container. This adds a container layer which allows modifications of the entire copy of the image.

7. What command can be used to create an image from a Dockerfile? 
docker build <path>

8. What command will start a docker container? 
To start a container from a docker image file you will use the following command:
 docker run [OPTIONS] IMAGE [COMMAND] [ARG...]

To start one or more stopped containers you use the following command:
 docker start [OPTIONS] CONTAINER [CONTAINER...]

9. What command will stop a docker container? 
To stop one or more running containers tou use the following command:
 docker stop [OPTIONS] CONTAINER [CONTAINER...]

10. What command will remove a docker container? Image? 
To remove one or more containers use the command:
 docker stop [OPTIONS] CONTAINER [CONTAINER...]

To remove one or more imagaes use the command:
 docker rmi [OPTIONS] IMAGE [IMAGE...]

11. What command will list all running docker containers? all containers? 
The command to list all running containers is:
 docker container ls

12. What command will list all docker images?
The command to list all docker images is:
 docker images ls

13. What command do you use to deploy docker containers using information in the dockercompose.yml file? 
The command you use to compile based off of the yml file is:
 docker compose up

14. How can you specify in the docker-compose.yml file that you want docker containers to use the
hosts network? 
In the .yml file you can specify "network_mode: host" to ensure your containers use the host network.

15. How can you specify in the docker-compose.yml file where the Dockerfile for a particular container
is found?
You specify where the Dockerfiles are in the "build: <file-path>" command under the "services" section
