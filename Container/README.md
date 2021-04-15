# Docker Configuration and Application Deployment

## About

This document will help you to configure docker in EC2 instance and deploy an application in the container.

## Prerequisite

- Amazon Linux EC2 instance (Minumum - t2.micro) in Public Subnet
- Docker Hub Account

### Bash commnads

- Login to EC2 instances created for this Lab and run the below commands.
``` bash
sudo amazon-linux-extras install docker
sudo service docker start
sudo usermod -a -G docker ec2-user
sudo yum install git
```
- After successfull execution of the above command, close the terminal/cmd and start the new terminal/cmd and execute the below commands.

```bash
git clone https://github.com/erkrvishal/aws-sa-training.git
cd aws-sa-training/Container/Docker/
docker build -t containerapp .
docker images --filter reference=containerapp
docker run -t -i -p 80:80 containerapp
```
- After executing docker run command, access the appication using the Public IP or Public DNS and you will be able to see the webpage.
- In below command pass the credentials for the Docker Hub Account and push the image in the docker hub registery.

```bash
docker login --username YOUR_USER
docker images
docker tag IMAGEID YOUR_USER/containerapp
docker push YOUR_USER/containerapp
```

## Possible Errors

- If you are facing difficulty in accessing the webpage, perform the below checks:
  - Check the Security Group attached to the Instance. It should allow the http inbound rule.
  - Check if the instance is launched in the Public Subnet or not
  - Check if the route table is having route out to Internet Gateway
  - Check if the Public Route table is having the subnet association in which you have provisoned the EC2 Instance
