# Ansible with Docker containers

This project contains a sample Ansible configuration to deploy (multiple) Angular apps as a docker container. 

## Getting started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

* Use the official Ansible documentation to [install](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) Ansible.

* Edit `ansible/hosts` with your remote hosts.

### Usage
Run the following command in the ansible folder:
```
ansible-playbook -i hosts site.yml
```
This will install docker, if it isn't already installed, and build Docker images of the Angular projects in the root. When the playbook is finished, the Angular projects are reachable by the ports 81 & 82.

### Notes
If you're using a CI/CD tool like CircleCI, you would probably already have a builded app on you job container. If that is the case, to speed up the process, you can copy the build folder instead of the whole project and skip the build steps of the Dockerfile. 

## License
[MIT](https://choosealicense.com/licenses/mit/)
