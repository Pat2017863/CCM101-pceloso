# Mission Reflection

## 1. Docker Containers vs Virtual Machines

Docker containers are faster to start than Virtual Machines because they do not need to install a complete operating system. Containers are also lighter and use fewer computer resources. In this activity, I was able to run an Nginx container quickly using Docker.

## 2. Port Mapping

Port mapping is needed so that we can access the web server running inside the container. The `-p 8080:80` command connects port 8080 on the computer to port 80 inside the container. This allowed me to access Nginx using `http://localhost:8080`.

## 3. docker rm

The `docker rm` command removes a stopped container from Docker. After removing the container, the container itself is no longer available. If the container is created again, it will be a new container.

## 4. Containerization and DevOps

Containerization helps developers and IT teams work together more easily. Developers can create an application in a container and IT teams can run the same container in different environments. This can make software deployment easier and more consistent.

## 5. GitHub Portfolio

My GitHub portfolio is improving as I add more cloud computing laboratory activities. In this laboratory, I added my Cloud-Native Engineer activity and documented my Docker commands and screenshots. This helps me keep my work organized and shows the skills I have learned in cloud computing.
