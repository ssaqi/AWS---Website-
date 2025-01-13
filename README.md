# How to Host a Website on AWS EC2 Using Apache  

## Introduction  
This guide explains how to create an AWS EC2 instance and configure it to host a website using Apache Web Server.  

## Prerequisites  
- AWS account  
- Basic knowledge of Linux commands  
- SSH client (e.g., Terminal or PuTTY)  

## Steps  
### 1. Launch an EC2 Instance  
1. Go to the AWS Management Console.  
2. Create an EC2 instance with Amazon Linux 2 or Ubuntu.  
3. Configure security groups to allow HTTP (port 80) and SSH (port 22).  

### 2. Connect to Your Instance  
Use the following command to connect via SSH:  
```bash
ssh -i your-key-file.pem ubuntu@your-instance-public-d

### 3. Install some files

sudo apt update && sudo apt install apache2 -y
sudo systemctl start apache2
sudo systemctl enable apache2

4. Deploy Your Project Using Git
After setting up the Apache server, follow these steps to deploy your project using Git:

Navigate to the Apache Web Server Directory:

bash Copy code
sudo cd /var/www/html/
Create a Directory for Your Projects:

bash
Copy code
sudo mkdir projects
Move into the Projects Directory:

bash Copy code
sudo cd projects/

Clone Your Git Repository:
Replace repo_name with the URL of your Git repository.

bash Copy code
sudo git clone repo_name

Move Project Files to the Root Directory:

Replace folder_name with the name of the folder cloned from the repository.

bash Copy code
sudo mv folder_name/* .
Test Your Deployment:

Access your project in the browser by entering the public IP of your EC2 instance.

Ensure the project files are served correctly by Apache.








