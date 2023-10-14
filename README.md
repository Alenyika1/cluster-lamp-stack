## Deployment and Configuration of Ubuntu Virtual Machines with Vagrant

## Introduction

This repository contains a Bash script designed to automate the deployment and configuration of two Ubuntu virtual machines using Vagrant. The primary purpose of this script is to establish a foundational LAMP (Linux, Apache, MySQL, PHP) stack and configure Nginx for load balancing to support web applications. This README provides an organized overview of the script's core functionality and how to utilize it effectively.

## Table of Content
- [Introduction](#introduction)
- [Requirements](#requirements)
- [Project Overview](#project-overview)
- [Usage Instructions](#usage-instructions)

## Requirements
To deploy the LAMP stack with load balancing project using Vagrant, you'll need the following:

1. Hardware Requirements:
   - A capable computer with enough CPU and RAM resources to run virtual machines.

2. Software Requirements:
   - An OS supported by Vagrant (Windows, macOS, or Linux).
   - Install Vagrant from the official website.
   - Virtualization software like VirtualBox.
   - A Bash-compatible shell on your local machine.

3. Project Files:
   - Download or clone the project files from the repository.

4. Internet Connection:
   - Ensure you have an internet connection for downloading necessary resources.

5. Project-Specific Requirements:
   - Ubuntu 20.04 virtual machine images are used by default. Make sure they are available or specify alternatives in the Vagrantfile.

6. Permissions:
   - Ensure you have the right permissions to create and configure virtual machines locally.

## Project Overview:

- Vagrant Configuration:
   - Initializes and provisions two Ubuntu virtual machines, named "master" and "slave."
   - Configures network settings to enable communication between the virtual machines.

- User and SSH Key Setup:
   - Creates a user account called "altschool" on the "master" virtual machine, granting it sudo privileges.
   ![Altschool User](./Screenshot/altschool.png)
   - Establishes SSH key-based authentication from the "master" to the "slave" virtual machine.
   ![ssh-key-setup](./Screenshot/ssh-key.png)

- Data Transfer:
   - Copies essential data and the SSH public key from the "master" to the "slave" virtual machine.
   - Facilitates data synchronization between the two virtual machines.
- Data Transfer:
   - Copies essential data and the SSH public key from the "master" to the "slave" virtual machine.
   - Facilitates data synchronization between the two virtual machines.

- LAMP Stack Installation:
- LAMP Stack Installation:
   - Installs Apache, MySQL, and PHP on both the "master" and "slave" virtual machines.

- Apache and MySQL Configuration:
   - Enables and secures Apache and MySQL on both virtual machines, including the use of the `mysql_secure_installation` script.

- Testing the LAMP Setup: 
   - Creates a PHP info file within the web directory on both virtual machines, serving as a verification of the LAMP stack configuration.
- Testing the LAMP Setup: 
   - Creates a PHP info file within the web directory on both virtual machines, serving as a verification of the LAMP stack configuration.

- Nginx Load Balancer Setup: 
   - Installs Nginx on the "master" virtual machine and configures it as a load balancer.
   - This setup helps distribute incoming web traffic evenly between the "master" and "slave" virtual machines, thereby optimizing resource utilization and providing fault tolerance.

## Usage Instructions

1. Ensure that Vagrant and VirtualBox are installed on your local machine.
2. Clone this repository to your local system.
3. Run the Bash script to deploy and configure the virtual machines:

![Usage Instruction](./cluster-lamp-stack/screenshot/lamp-stack.png)
