# BootStrap Code for application deployment

## About
This document will help to deploy the application into the Ec2 Instance.

## BootStrap Script

```bash
#!/bin/bash
yum update -y
yum install -y git httpd php
cd /var/www/html
wget https://raw.githubusercontent.com/erkrvishal/aws-sa-training/master/Instance_lab/dog.jpg
wget https://raw.githubusercontent.com/erkrvishal/aws-sa-training/master/Instance_lab/index.php
systemctl start httpd
systemctl enable httpd
```

