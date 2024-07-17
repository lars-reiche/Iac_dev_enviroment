# Setup dev_enviroment
By using Docker Dev Containers, we ensure a clean and consistent development environment. In VS Code, we use Docker Dev Containers to install and deploy the necessary dependencies in a separate local container. The Dev Container is located directly in the project folder so that every developer can work with it in a standardized way and directly from the project. Another advantage is that local installations and versions are not changed. Docker Dev Containers therefore offer a solution integrated into VS Code for providing a standardized virtual development environment without burdening the actual system.

## Table of Content
1. [Requirements](#requirements)
1. [Dev_Containers](#dev_container)
2. [Start Container](#start_container)

## Requirements
Make sure that the following software is installed locally on your computer. 
- [VS-Code](https://code.visualstudio.com/)
- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
    - sign up (with your github Account)
- [Git](https://git-scm.com/)
    - Git Config
    ```shell
    git config --global user.email "your.mail@edeka.de"
    git config --global user.name "user-name"
    ```

## Dev_Container
### 1. Folder Structure
- project folder
    - .devcontainer (folder)
        - devcontainer.json
    - requirements.txt
    - project files

### 2. Setup

1. create folders and files as above
2. config devcontainer.json
    ```json
        {
    "name": "ki-cc devcontainers",
    "image": "mcr.microsoft.com/devcontainers/base:ubuntu",
    "extensions": [
        "ms-azuretools.vscode-bicep",
        "prompt-flow.prompt-flow",
        "esbenp.prettier-vscode",
        "ms-python.python"
    ],
    "postCreateCommand": "sudo apt-get update && sudo apt-get install -y git python3.12 && pip install -r /workspace/requirements.txt",
    "settings": {
        "python.pythonPath": "/usr/bin/python3.12"
    }
    }
    ```
    Define VS-Code extentions, python version, requierments and more. 



## Start_Container
1. Add Dev Containers Extention to your local VS-Code
2. Pull this git repo
     ```shell
    ---
    ```
3. Check Docker is running

    ```docker
    docker info
    docker --version
    ```
    alternative: 
    open Docker Desktop and check manualy

4. Start Container
    1. Pres CMD+Shift+P
    2. type and select "Dev Container: Reopen in Container"

The Dev Container starts.
It may take a few seconds to start. 
The VS code window refreshes on startup. It may be that the authorization to write must be given at the first start. In this case, a pop-up window with selection options appears. Press accept here.
test