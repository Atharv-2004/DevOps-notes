# Software Engineering – Docker Revision Notes  
**Date:** 12 November 2025

Docker is a platform that helps developers automate the deployment, management, scaling, and operation of applications using containers. In this class, the emphasis was on understanding Docker’s core capabilities such as image creation, Dockerfile usage, and command-line operations for managing containers.

Docker works around two primary building blocks: images and containers. A Docker image can be understood as a packaged runtime environment that contains the application along with all dependencies required for execution. Images act as the blueprint from which containers are created. A Docker container is a running instance of an image. While it may resemble a virtual machine in behavior, it is much lighter because it shares the host operating system’s kernel, resulting in faster startup and better resource efficiency.

Several essential Docker commands were discussed. The `docker build` command is used to create images from a Dockerfile. While building images, tags are assigned using the `-t` option, and these tags must follow lowercase naming conventions. The `docker run` command is used to start containers from images and supports options such as `-d` for running containers in detached mode and `-p` for mapping container ports to host ports.

A Dockerfile is a structured set of instructions used to construct Docker images. The `FROM` instruction defines the base image on which the new image is built. The `RUN` instruction executes commands during the image build process, and each `RUN` instruction creates a new image layer, which can affect image size and build performance if not managed carefully. The `CMD` and `ENTRYPOINT` instructions define the default behavior when a container starts. While both specify startup commands, `CMD` can be overridden at runtime, whereas `ENTRYPOINT` enforces execution and is not easily overridden.

Advanced Docker concepts were also covered. Multi-stage builds were introduced as a method to optimize image size by separating build-time and runtime dependencies. This approach ensures that only essential components are included in the final image. The Copy-on-Write (CoW) mechanism was explained as an optimization technique that allows Docker to load only required layers into memory, improving runtime efficiency.

Performance optimization strategies focused on minimizing the number of image layers by combining commands where possible. Reducing layers helps improve container performance and reduces image size. Base image selection was highlighted as another critical factor. For example, using a JRE instead of a JDK in production environments for Java applications significantly reduces image size and improves deployment efficiency.

A practical demonstration involved creating a Docker image for a Java application using a multi-stage build. The build stage used a JDK to compile the application, while the final runtime stage used a JRE to produce a smaller and more efficient production image.

The class also guided students through setting up a Docker environment, creating containers, and deploying applications. Emphasis was placed on hands-on practice to reinforce understanding of Docker commands and workflows.

Overall, the session provided a thorough overview of Docker concepts, image creation techniques, and best practices for container management. These concepts form an important foundation for software engineers working with modern deployment pipelines and container-based systems.
