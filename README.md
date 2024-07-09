# IaC to setup dev_enviroment

Introduction

## Table of Content
1. [Installations](#installations)
1. [MacOS](#macos)
2. [Windows](#windows)
3. [Docker](#docker)
4. [Individual Setup](#individual)

## Installations
1. Python 3.12
2. Git 2.45.2
3. VS-Code with:
    - Bicep
    - Promt Flow
    - Prettier
    - Python
4. Azure Storage Explorer
5. Miro

## MacOS
1. install Homebrew

    ```shell
    d/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```
2. install Ansible using Homebrew
    ```shell
    brew install ansible
    ```
3. run Ansible playbook
    > **Hint:** The password you are asked for is that of your local computer. 
    ```shell
    ansible-playbook -i admin, --user admin macos_playbook.yml -K
    ```
    
    1. If the installation of VS-Code extensions fails.
        - open VS-Code
        - press CMD+Shift+P
        - type "Shell Command"
        - select "install 'code' command to PATH"
        - run Ansible playbook again
    2. customization

        Shell command may require customization for installation on specific users.
        ```shell
        ansible-playbook -i "your-user", --user "your-user" macos_playbook.yml -K
        ```

## Windows
...

## Customization

1. Git Config
    ```shell
    git config --global user.email "your.mail@edeka.de"
    git config --global user.name "user-name"
    ```
