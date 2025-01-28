## Docker Setup
You can find info about the images used in this repo [here](https://github.com/soham2560/DockerForROS2Development)
<!-- For Linux -->
### For Linux
- For Linux, run the following commands in the terminal

```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh

sudo groupadd docker
sudo usermod -aG docker $USER
newgrp docker
```

### Test your Docker installation

```bash
docker run hello-world
```

### Check Docker version

```bash
docker --version
```

### Try pulling a public image

```bash
docker pull ubuntu:jammy

docker run -it ubuntu:jammy bash
```

## `humble-garden` image
- To pull latest docker image
    ```bash
    docker pull ghcr.io/soham2560/humble-garden:latest
    ```
- To start container
    - Open this repo
    - Open Command Pallete with `Ctrl+Shift+P`
    - Select Option to Rebuild and Reopen Container
    - You can use `Import Libs` button once container has opened to import dependent libs
    - Use `Build WS` button to build workspace

Note: To access these buttons you may need to enable [VSCode Action Button Extension](https://marketplace.visualstudio.com/items?itemName=seunlanlege.action-buttons) through the Extensions Tab in VSCode, the extension should download automatically on container startup

### This work is also inspired by the work of [rahulkatiyar19955](https://www.rahulkatiyar.com/) and some work I did at [MIT Tech Team](https://github.com/mittechteam), head over to his profile if you want to see some more cool robotics work.
