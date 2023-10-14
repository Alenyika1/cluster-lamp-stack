**Deployment and Configuration of Ubuntu Virtual Machines with Vagrant**

This repository contains a Bash script for deploying and configuring two Ubuntu virtual machines using Vagrant. The script automates the setup of a basic LAMP stack and Nginx load balancing for web applications. Below is an overview of the script's functionality:

## Table of Contents

- [Introduction](#introduction)
- [Project Overview](#project-overview)
- [Specifications](#specifications)
- [Prerequisites](#prerequisites)
- [Instructions](#instructions)


##  Vagrant Configuration:
   - Initializes and provisions two Ubuntu virtual machines: "master" and "slave."
   - Configures network settings to enable communication between the virtual machines.

##  User and SSH Key Setup:
   - Creates a user named "altschool" with root (sudo) privileges on the "master" virtual machine.
   - Sets up SSH key-based authentication from the "master" to the "slave" virtual machine.

##  Data Transfer:
   - Copies data and an SSH public key from the "master" to the "slave" virtual machine.
   - Enables data synchronization between the virtual machines.

##  LAMP Stack Installation:
   - Installs Apache, MySQL, and PHP on both the "master" and "slave" virtual machines.

##  Apache and MySQL Configuration:
   - Enables and secures Apache and MySQL on both virtual machines using the `mysql_secure_installation` script.

##  Testing the LAMP Setup:
   - Creates a PHP info file in the web directory on both virtual machines to verify the LAMP stack configuration.

##  Nginx Load Balancer Setup:
   - Installs Nginx on the "master" virtual machine.
   - Configures Nginx as a load balancer to distribute incoming web traffic between the "master" and "slave" virtual machines.

##  Cleanup:
   - Removes temporary files and configurations created during the setup process.
   - Enables SSH key-based authentication from the "master" to the "slave."

##  Data Transfer (continued):
   - Continues to synchronize data between the "master" and "slave" virtual machines.

##  Completion Message:
   - Displays a completion message indicating the successful deployment.

## Usage Instructions:
1. Ensure Vagrant and VirtualBox are installed on your system.
2. Clone this repository and navigate to the project directory.
3. Run the Bash script to deploy and configure the virtual machines:

   ```bash
   ./lamp-stack.sh
   ```

Please note that this script provides a foundation for setting up a basic LAMP stack and load balancing using Nginx. Customize the script to suit your specific requirements and security needs. Always exercise caution when executing scripts that modify system configurations, and ensure that you have the necessary permissions for these operations.
