# project-docker2-cbdas
🔷 Installing and Configuring Docker on AWS EC2 Instance

This task involves setting up Docker, a containerization platform, on a virtual server created using Amazon EC2 (Elastic Compute Cloud) from Amazon Web Services (AWS)
.

🔶 Overview

Amazon EC2 provides scalable cloud-based virtual machines, while Docker allows applications to run inside lightweight containers. Installing Docker on an EC2 instance enables efficient deployment, testing, and management of applications in isolated environments.

🔶 Steps Involved
1. Launch EC2 Instance
Log in to AWS console
Choose EC2 service
Launch a new instance (e.g., Amazon Linux or Ubuntu)
Configure security groups (allow SSH – port 22)
2. Connect to Instance
Use SSH to connect:
ssh -i your-key.pem ec2-user@your-public-ip
3. Update System Packages
sudo yum update -y     # Amazon Linux

or

sudo apt update -y     # Ubuntu
4. Install Docker
sudo yum install docker -y

or

sudo apt install docker.io -y
5. Start Docker Service
sudo systemctl start docker

Enable Docker on boot:

sudo systemctl enable docker
6. Add User to Docker Group
sudo usermod -aG docker ec2-user
7. Verify Installation
docker --version
docker run hello-world
🔶 Outcome
Docker is successfully installed and running
Containers can be created and managed on EC2
Enables deployment of applications in isolated environments
