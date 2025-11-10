# Docker and Containerization – Class Revision Notes  
**Date:** 10 November 2025

Docker is an open platform used for building, packaging, and running applications. It allows applications to be separated from the underlying infrastructure, enabling faster and more consistent software delivery. Using Docker, infrastructure can be managed in a manner similar to application code.

Applications are executed inside containers. Containers bundle an application together with all required dependencies such as libraries and configurations. This approach ensures that applications behave consistently across different environments, regardless of where they are deployed.

To start working with containers, Docker provides a set of core commands. The `docker run` command is used to create and start a new container. For example, running `docker run -it ubuntu bash` launches an Ubuntu container and provides interactive terminal access. To execute commands inside an already running container, the `docker exec` command is used. This allows users to open a shell or run commands without restarting the container.

Running containers can be monitored using `docker ps`, which lists active containers. Detailed information about a container, including networking details such as its IP address, can be obtained using `docker container inspect <container_id>`.

Docker images act as templates from which containers are created. A common workflow involves starting from an existing image, making changes inside a running container, and then saving those changes as a new image using `docker commit`. Available images on a system can be viewed using `docker images`. New images can be created from containers using `docker commit -m "message" <container_id> <new_image_name>`.

Images can be uploaded to Docker Hub using the `docker push <image_name>` command. To successfully push an image, the image name must begin with the user’s Docker Hub username, ensuring correct ownership and access.

Container communication often requires knowing the container’s IP address. Docker allows inspection of containers to retrieve this information. Once the IP address is known, tools such as `curl` can be used to interact with services running inside containers.

Docker images are commonly built using a Dockerfile. A Dockerfile defines a sequence of build steps, where each instruction creates a new image layer. Understanding image layers is important because Docker caches these layers, improving build efficiency and reducing redundant work.

Containers can be run in either attached or detached modes. Using the `-d` flag with `docker run` starts a container in detached mode, allowing it to run in the background without occupying the terminal.

Docker uses a layered filesystem approach. Each modification made to an image and committed results in a new layer that contains only the changes. This layered design contributes to Docker’s efficiency and reusability.

Compared to virtual machines, Docker containers are more resource-efficient. Containers do not include a full operating system, as they share the host system’s kernel. This reduces overhead and improves performance. However, Docker usage across different CPU architectures, such as ARM and AMD, can introduce compatibility challenges, making architecture consistency important during image creation and deployment.

Docker provides a flexible and efficient solution for developing, testing, and deploying applications. Its container-based approach supports debugging, local development, and production deployments, making it a key tool in modern software engineering workflows.
