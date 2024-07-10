# IaC to setup dev_enviroment

To ensure a standardized and scalable provision of our development environment, we use the principles of Infrastructure as Code (IaC). We rely specifically on Ansible.

Ansible enables us to define our infrastructure in code and ensure that the desired configurations and states are consistent and reproducible. It is based on the desired end state, which means that the previously defined end state is aimed for and achieved by executing the Ansible code. This greatly simplifies the management and automation of complex environments and ensures that all systems have exactly the configuration we need.

## Table of Content
1. [Installations](#installations)
1. [MacOS](#macos)
2. [Windows](#windows)
3. [Docker](#docker)
4. [Customization](#customization)

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
4. [Individual Setup](#customization)

## Windows
...

## Customization

1. Git Config
    ```shell
    git config --global user.email "your.mail@edeka.de"
    git config --global user.name "user-name"
    ```
