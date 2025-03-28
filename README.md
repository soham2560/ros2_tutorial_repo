
# Dev Container Setup for ROS2 Development

## Acknowledgment

If you are using this repository or any of its derivatives, please  **cite it appropriately** . The Docker images used in this repository originate from [DockerForROS2Development](https://github.com/soham2560/DockerForROS2Development).

## Overview

This repository provides a **VS Code Dev Container** setup for  **ROS2 Humble development** , leveraging Docker to create an isolated, reproducible development environment. It integrates the **Docker images** from [this repo](https://github.com/soham2560/DockerForROS2Development) into a **Dev Container** for seamless development in VS Code.

## Prerequisites

Ensure you have the following installed:

* **Docker** : Follow the steps below to install it.
* **VS Code** : Download and install from [here](https://code.visualstudio.com/).
* **Dev Containers Extension** : Install the [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension in VS Code.

---

## Installation Guide

### Installing Docker (Linux)

Run the following commands in the terminal:

```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh

sudo groupadd docker
sudo usermod -aG docker $USER
newgrp docker
```

Verify Docker installation:

```bash
docker run hello-world
```

### Setting Up the Dev Container

1. **Clone this repository** :

```bash
   git clone https://github.com/YOUR_REPO_NAME.git
   cd YOUR_REPO_NAME
```

1. **Open in VS Code** :

* Open  **VS Code** .
* Navigate to **File > Open Folder** and select this repository.

1. **Open in Dev Containers** :

* Open the **Command Palette** (`Ctrl+Shift+P`).
* Search for **"Rebuild and Reopen in Container"** and select it.
* VS Code will automatically build and open the container.

1. **Using the Development Tools** :

* Click **Import Libs** to fetch dependencies.
* Click **Build WS** to compile the ROS2 workspace.

> **Note:** These features require the following VS Code extensions:
>
> * [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
> * [Action Button](https://marketplace.visualstudio.com/items?itemName=seunlanlege.action-buttons)

---

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

---

## Credits

This work is built on the Docker images provided by [soham2560/DockerForROS2Development](https://github.com/soham2560/DockerForROS2Development). This repository extends that work by  **integrating it with Dev Containers for a streamlined ROS2 development experience** .

For more information, check out projects from:

* [rahulkatiyar19955](https://www.rahulkatiyar.com/)
* [MIT Tech Team](https://github.com/mittechteam)
