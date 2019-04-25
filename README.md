HOW CONTAINERS WORK WITH THE APPLICATION
============
Container Basics
-------------
An application container is a stand-alone package for a software application that comprises of application binaries, software dependencies and the hardware requirements needed to run the application in a single unit

Why Containers
-------------
* The container works as a self isolated unit that can run anywhere that supports it
* The container retains it's identity regardless of the operating system it is running on. This helps ensure that the container will run on different servers.
* Containers implement micro service architecture, where each microservice comprises of a number of containers, both master and slave.This makes application deployment easy by the engineering teams.

Docker as a containerization tool for the Converge Application
------------
Docker is one of the most widely used containerization technologies because it is open source and works across a number of platforms.
Converge as an application that manages meeting rooms for Andela Uganda was containerized using Docker which helps consume fewer resources than a comparable deployment on virtual machines because containers share resources without a full operating system to underpin each app.
Converge comprises of the frontend service, backend service and mobile service. All these were containerized using Docker in order to reap from the benefits of Docker
--------  -----------------------
The Docker Architecture
--------  -----------------------
![Alt text](images/dockerArch.png)

The Docker architecture uses a client-server model and comprises of the Docker Client, Docker Host, Network and Storage components, and the Docker Registry/Hub. 

The Docker Client
-----------------
The Docker client enables users to interact with Docker. The Docker client can reside on the same host as the daemon or connect to a daemon on a remote host. A docker client can communicate with more than one daemon. The Docker client provides a command line interface (CLI) that allows you to issue build, run, and stop application commands to a Docker daemon.

The main purpose of the Docker Client is to provide a means to direct the pull of images from a registry and to have it run on a Docker host. Common commands issued by a client are:

* docker build
* docker pull
* docker run

The DockerHost
------------------
The Docker host provides a complete environment to execute and run applications. It comprises of the Docker daemon, Images, Containers, Networks, and Storage. As previously mentioned, the daemon is responsible for all container-related actions and receives commands via the CLI or the REST API. It can also communicate with other daemons to manage its services. The Docker daemon pulls and builds container images as requested by the client. Once it pulls a requested image, it builds a working model for the container by utilizing a set of instructions known as a build file. The build file can also include instructions for the daemon to pre-load other components prior to running the container, or instructions to be sent to the local command line once the container is built.

Docker Objects
Various objects are used in the assembling of your application. The main requisite Docker objects are:


The following screenshots illustrate the use of Docker within the three Converge applications
--------  -----------------------
The Front End
--------  -----------------------
![Alt text](images/dockerfront.png)

The Docker file
![Alt text](images/Dockerfile.png)
--------  -----------------------
--------  -----------------------
The Back End
--------  -----------------------
![Alt text](images/dockerfront.png)

The Docker file
![Alt text](images/Dockerfile.png)
--------  -----------------------
--------  -----------------------
The Mobile Application
--------  -----------------------
![Alt text](images/dockerfront.png)

The Docker file
![Alt text](images/Dockerfile.png)
--------  -----------------------
