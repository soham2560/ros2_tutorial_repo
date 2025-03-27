# Docker Setup for ROS2 Development

## Acknowledgment
If you are using this repository or any of its derivatives, please make sure to **cite** it appropriately.

## Overview
This repository provides a streamlined Docker setup for ROS2 development. The Docker images used in this repository are detailed [here](https://github.com/soham2560/DockerForROS2Development).

## Prerequisites
Ensure that Docker is installed on your system. Follow the steps below to set it up if you haven't already.

---

## Installation Guide

### Installing Docker (Linux)
Run the following commands in the terminal to install Docker:

```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh

sudo groupadd docker
sudo usermod -aG docker $USER
newgrp docker
```

### Verify Docker Installation
To check if Docker is installed correctly, run:

```bash
docker run hello-world
```

### Check Docker Version
To confirm your Docker version:

```bash
docker --version
```

### Pull and Run a Public Docker Image
Try pulling and running a sample Ubuntu image:

```bash
docker pull ubuntu:jammy

docker run -it ubuntu:jammy bash
```

---

## Using the `humble-garden` Docker Image
This repository provides a preconfigured Docker image for ROS2 Humble development.

### Pull the Latest Image

```bash
docker pull ghcr.io/soham2560/humble-garden:latest
```

### Starting the Container
1. Open this repository in **VS Code**.
2. Open the **Command Palette** using `Ctrl+Shift+P`.
3. Select the option **Rebuild and Reopen Container**.
4. Once the container is open:
   - Click the **Import Libs** button to import dependencies.
   - Click the **Build WS** button to build the workspace.

> **Note:** To access these features, ensure you have installed and enabled the following VS Code extensions:
> - [Dev Containers Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
> - [Action Button Extension](https://marketplace.visualstudio.com/items?itemName=seunlanlege.action-buttons)

---

## Credits
This work is inspired by the contributions of [rahulkatiyar19955](https://www.rahulkatiyar.com/) and additional work done at the [MIT Tech Team](https://github.com/mittechteam). Check out their profiles for more exciting robotics projects!
