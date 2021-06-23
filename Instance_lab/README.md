# BootStrap Code for application deployment

## About
This document will help to deploy the application into the Ec2 Instance.

## BootStrap Script

```bash
sudo yum update -y
sudo yum install -y git httpd php
cd /var/www/html
sudo https://raw.githubusercontent.com/erkrvishal/aws-sa-training/master/Instance_lab/dog.jpg
sudo wget https://raw.githubusercontent.com/erkrvishal/aws-sa-training/master/Instance_lab/index.php
sudo systemctl start httpd
sudo systemctl enable httpd
```

