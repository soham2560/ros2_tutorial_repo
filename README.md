
# ROS2 + Docker + VSCode Dev Containers

## Overview

This repository provides you template for robotics development cycle using ROS2 and leveraging the capabilities of Docker with VS Code Dev Container. The basis for all the work done here are taken from [DockerForROS2Development](https://github.com/soham2560/DockerForROS2Development).

## Prerequisites

- Ubuntu 22.04 or 24.04
- VSCode
- Remote Development Extension by Microsoft (Inside VSCode)
- **Docker Installation**
  ```bash
  # Install Docker using convenience script
  curl -fsSL https://get.docker.com -o get-docker.sh
  sudo sh ./get-docker.sh

  # Post-install configuration
  sudo groupadd docker
  sudo usermod -aG docker $USER
  sudo systemctl enable docker.service
  sudo systemctl enable containerd.service

  # Verify installation
  sudo systemctl is-enabled docker
  ```
- **Reboot before proceeding further**

Verify Docker installation:

```bash
docker run hello-world
```

### Setting Up the Dev Container

- **Clone this repository** :

    ```bash
    mkdir ros2_ws && cd ros2_ws
    # Clone the repo
    https://github.com/soham2560/ros2_tutorial_repo .
    # Open VSCode 
    code .
    ```

- **To enter the container**
    - Open Command Pallete with `Ctrl+Shift+P`
    - Select **Dev Containers: Rebuild and Reopen in Container**


## Working with ROS

- **Open two Terminals**
- **Check ROS Humble Installation**
  ```bash
  # In one Terminal
  ros2 run demo_nodes_cpp talker
  ```

  ```bash
  #In another Terminal
  ros2 run demo_nodes_py listener
  ```
- You should see communication between the nodes if everything is working correctly.

## Dev Container Configuration

This repository provides the following pre-configured  **Dev Container setup** :

* **`devcontainer.json`** : Defines the VS Code Dev Container environment.
* **`Dockerfile`** : Builds the container using the **Humble Garden** Docker image.
* **Preinstalled Extensions** :
* ROS2 Development Tools
* Docker Support
* C++ & Python Development Tools
* YAML & XML Support

For advanced customization, edit the `devcontainer.json` file.


## Credits

This work is built on the Docker images provided by [soham2560/DockerForROS2Development](https://github.com/soham2560/DockerForROS2Development). This repository extends that work by  **integrating it with Dev Containers for a streamlined ROS2 development experience** .

For more information, check out projects from:

* [rahulkatiyar19955](https://www.rahulkatiyar.com/)
* [MIT Tech Team](https://github.com/mittechteam)
