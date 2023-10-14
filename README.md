## Deployment and Configuration of Ubuntu Virtual Machines with Vagrant## 

## Introduction:## 

This repository contains a Bash script designed to automate the deployment and configuration of two Ubuntu virtual machines using Vagrant. The primary purpose of this script is to establish a foundational LAMP (Linux, Apache, MySQL, PHP) stack and configure Nginx for load balancing to support web applications. This README provides an organized overview of the script's core functionality and how to utilize it effectively.

## Table of Content
- [Introduction](#introduction)
- [Requirements](#requirements)
- [Project Overview](#project-overview)
- [Usage Instructions](#usage-instructions)
- [Customization](#customisation)

## Requirements
To deploy the LAMP stack with load balancing project using Vagrant, you'll need the following:

**1. Hardware Requirements:**
   - A capable computer with enough CPU and RAM resources to run virtual machines.

**2. Software Requirements:**
   - An OS supported by Vagrant (Windows, macOS, or Linux).
   - Install Vagrant from the official website.
   - Virtualization software like VirtualBox.
   - A Bash-compatible shell on your local machine.

**3. Project Files:**
   - Download or clone the project files from the repository.

**4. Internet Connection:**
   - Ensure you have an internet connection for downloading necessary resources.

**5. Project-Specific Requirements:**
   - Ubuntu 20.04 virtual machine images are used by default. Make sure they are available or specify alternatives in the Vagrantfile.

**6. Permissions:**
   - Ensure you have the right permissions to create and configure virtual machines locally.

**7. Customization (Optional):**
   - Customize components like Apache, MySQL, PHP, and Nginx if needed.

**8. Security Considerations:**
   - Implement security practices post-deployment to safeguard your virtual machines and hosted applications.

Always refer to the official documentation for the software involved and adhere to best practices for system security and management.
## Project Overview:

- Vagrant Configuration:
   - Initializes and provisions two Ubuntu virtual machines, named "master" and "slave."
   - Configures network settings to enable communication between the virtual machines.

- User and SSH Key Setup:## 
   - Creates a user account called "altschool" on the "master" virtual machine, granting it sudo privileges.
   - Establishes SSH key-based authentication from the "master" to the "slave" virtual machine.

- Data Transfer:
   - Copies essential data and the SSH public key from the "master" to the "slave" virtual machine.
   - Facilitates data synchronization between the two virtual machines.

- LAMP Stack Installation:
   - Installs Apache, MySQL, and PHP on both the "master" and "slave" virtual machines.

- Apache and MySQL Configuration:
   - Enables and secures Apache and MySQL on both virtual machines, including the use of the `mysql_secure_installation` script.

- Testing the LAMP Setup: 
   - Creates a PHP info file within the web directory on both virtual machines, serving as a verification of the LAMP stack configuration.

- Nginx Load Balancer Setup: 
   - Installs Nginx on the "master" virtual machine and configures it as a load balancer.
   - This setup helps distribute incoming web traffic evenly between the "master" and "slave" virtual machines, thereby optimizing resource utilization and providing fault tolerance.

- Cleanup:
   - Removes temporary files and configurations generated during the setup process.
   - Ensures SSH key-based authentication from the "master" to the "slave" virtual machine remains enabled.

- Completion Message:## 
   - Concludes the deployment process by displaying a message confirming the successful setup.

## Usage Instructions:## 

1. Ensure that Vagrant and VirtualBox are installed on your local machine.
2. Clone this repository to your local system.
3. Run the Bash script to deploy and configure the virtual machines:

   ```bash
   ./lamp-stack.sh
   ```

Please keep in mind that this script forms the foundation for creating a basic LAMP stack and setting up Nginx for load balancing. It can be tailored to meet your specific needs and security considerations. Exercise due caution when executing scripts that modify system configurations, and always ensure you have the appropriate permissions for the operations being performed.