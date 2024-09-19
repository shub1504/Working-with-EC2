# DOCKER 
Docker is an open-source platform designed to automate the deployment, scaling, and management of applications using containerization. Containers are lightweight, portable units that bundle an application with all its dependencies, ensuring that it runs consistently across different environments, whether on a developer’s laptop, a test server, or in production. Docker revolutionizes software development by using containers to package and isolate applications and their dependencies. This ensures consistent performance across different environments, from development to production. Docker containers are lightweight, fast, and portable, and they make modern practices like microservices architecture, CI/CD, and multi-environment development easier to manage. Docker's ecosystem, including Docker Hub, Docker Compose, and orchestration tools like Docker Swarm, further enhances its capabilities for building scalable and efficient applications.

# Key Concepts of Docker:
**1.Docker Containers:**
A Docker container is an isolated, lightweight environment where an application runs. Unlike virtual machines (VMs), containers share the host machine’s operating system (OS) kernel but keep the application and its dependencies in separate environments. This isolation ensures that different applications can run on the same system without interfering with one another.

**2. Docker Images:**
A Docker image is a blueprint for creating containers. It’s a read-only template that contains the application code, libraries, environment variables, and configuration files necessary to run the application. Containers are created from Docker images.

**3. Dockerfile:**
A Dockerfile is a script containing a series of instructions that Docker uses to build an image. It specifies how the image is constructed, including what base image to use, which files to copy, which dependencies to install, and how to configure the container when it starts.

 <Common Instructions in a Dockerfile:>
* FROM: Defines the base image to use (e.g., FROM ubuntu:20.04).
* COPY or ADD: Copies files or directories from the local filesystem to the image.
* RUN: Executes commands to install software, update packages, or configure the environment.
* CMD: Specifies the default command to run when a container starts.
* EXPOSE: Declares which port the application will listen on (e.g., EXPOSE 8080).

**4. Docker Hub:**
Docker Hub is a cloud-based registry where developers can store and share Docker images. It offers a vast collection of pre-built images (e.g., operating systems, databases, programming languages) that can be pulled and used as the base for building new containers.

**5. Docker Engine:**
Docker Engine is the core part of the Docker platform that creates, runs, and manages containers. It is available in two editions:
* Docker Community Edition (CE): Free and open-source, suitable for developers and small teams.
* Docker Enterprise Edition (EE): Provides additional security, management, and support features for large-scale enterprise environments.

# Use Cases of Docker:
1. Development Environment: Docker makes it easy for developers to set up consistent development environments across teams. Developers can run containers locally that mirror the production environment.
2. Microservices: Docker is commonly used in microservices architecture, where applications are divided into smaller, independent services. Each service runs in its container, ensuring isolation and scalability.
3. Continuous Integration/Continuous Deployment (CI/CD): Docker containers are frequently used in CI/CD pipelines to ensure that applications are built and tested in consistent environments.

# STEPS TO INSTALL DOCKER 
To install Docker using PuTTY, you'll typically be connecting to a remote server running Linux (most commonly Ubuntu). PuTTY is used to establish an SSH connection to the server. Once you're logged in, the installation of Docker can be done using terminal commands.

Step 1: Connect to the Server via PuTTY
* Open PuTTY
* Enter the Hostname or IP Address
* Click Open
* Login to the server 

Step 2: Update Package Index
Once logged into the server, run the following commands to update the package index:

                    sudo apt-get update

Step 3: Install Prerequisites
To ensure Docker can be installed, you'll need to install a few prerequisite packages:

           sudo apt-get install apt-transport-https ca-certificates curl software-properties-common

Step 4: Add Docker’s Official GPG Key
Download Docker’s GPG key to verify the Docker packages are legitimate:

       curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

Step 5: Add the Docker APT Repository
Add Docker’s official repository to your system’s list of APT sources:

    echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

Step 6: Install Docker

          sudo apt-get install docker-ce docker-ce-cli containerd.io

Step 7: Verify Docker Installation
To verify that Docker is installed correctly, run the following command:

      docker --version

This will display the installed version of Docker. To further verify, you can run a simple test container:

      sudo docker run hello-world

If Docker is installed correctly, this command will download and run a test container, outputting a "Hello from Docker" message.










