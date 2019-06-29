# Ansible with Docker containers

This project contains a sample Ansible configuration to deploy (multiple) Angular apps as a docker container. 

## Getting started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

* Use the official Ansible documentation to [install](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) Ansible.

* Edit `ansible/hosts` with your remote hosts.

### Usage
* Run the following command in the ansible folder:
```
ansible-playbook -i hosts site.yml
```
This will install docker, if it isn't already installed, and build Docker images of the Angular projects in the root. When the playbook is finished, the Angular projects are reachable by the ports 81 & 82.

### Notes
Currently the Dockerfile includes a container which build the Angular project. When using a CI/CD tool - for example CircleCI - probably the build already exist on the job container. Change the roles so that the dist folder will be copied and the build process in the Dockerfile can be skipped.   

## License
[MIT](https://choosealicense.com/licenses/mit/)