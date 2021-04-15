# BootStrap Code for application deployment

## About
This document will help to deploy the application into the Ec2 Instance.

## BootStrap Script

```bash
sudo yum update -y
sudo yum install -y git httpd php
cd /var/www/html
sudo wget https://github.com/erkrvishal/aws-sa-training/Instance_lab/dog.jpg
sudo wget https://github.com/erkrvishal/aws-sa-training/Instance_lab/index.php
sudo systemctl start httpd
sudo systemctl enable httpd
```

