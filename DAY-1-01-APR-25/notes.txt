#!/bin/bash 
#update
sudo yum update -y
#install java
sudo yum install java-17-amazon-corretto -y
# Add the Jenkins Repository
sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo
#Import a key file from Jenkins
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
#Install Jenkins
sudo yum install jenkins -y
#Enable Jenkins
sudo systemctl enable jenkins
#start jenkins
sudo systemctl start jenkins
