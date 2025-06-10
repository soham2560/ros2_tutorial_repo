
# ROS2 + Docker + VSCode Dev Containers

## Overview
This repository provides a **VS Code Dev Container** setup for  **ROS2 Humble development** , leveraging Docker to create an isolated, reproducible development environment. It integrates the **Docker images** from [DockerForROS2Development](https://github.com/soham2560/DockerForROS2Development) repo into a **Dev Container** for seamless development in VS Code.

## Prerequisites

* **Ubuntu** (preferred)
* **VS Code** : Download and install from [here](https://code.visualstudio.com/download).
* **Dev Containers Extension** : Install the [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension in VS Code.

- **Docker Installation**
  ```bash
  # Install Docker using convenience script
  curl -fsSL https://get.docker.com -o get-docker.sh
  sudo sh ./get-docker.sh

  # Post-install configuration
  sudo groupadd docker
  sudo usermod -aG docker $USER
  ```
- **Reboot before proceeding further**

Verify Docker installation:

```bash
docker run hello-world
```

### Setting Up the Dev Container

- **Clone this repository** :

    ```bash
    https://github.com/soham2560/ros2_tutorial_repo 
    # Navigate to ros2_tutorial_repo directory and open VSCode 
    code .
    ```

- **To enter the container**
  * Open the **Command Palette** (`Ctrl+Shift+P`).
  * Search for **"Rebuild and Reopen in Container"** and select it.
  * VS Code will automatically build and open the container.

* **Using the Development Tools** :

  * Click **Import Libs** to fetch dependencies.
  * Click **Build WS** to compile the ROS2 workspace.

> **Note:** These features require the following VS Code extensions:
> * [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
> * [Action Button](https://marketplace.visualstudio.com/items?itemName=seunlanlege.action-buttons)


## Working with ROS

- **Open two Terminals**
- **Check ROS Humble Installation**
  ```bash
  # In one Terminal
  ros2 run demo_nodes_cpp talker
  ```

  ```bash
  # In another Terminal
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

This work is built on the Docker images provided by [soham2560/DockerForROS2Development](https://github.com/soham2560/DockerForROS2Development). This repository extends that work by  **integrating it with Dev Containers for a streamlined ROS2 development experience**.

For more information, check out projects from:

* [rahulkatiyar19955](https://www.rahulkatiyar.com/)
* [MIT Tech Team](https://github.com/mittechteam)
