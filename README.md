# Cloud DevOps Engineer Capstone Project

## Overview

In this project I applied the skills and knowledge which were developed throughout the Cloud DevOps Nanodegree program. These included:

- Working in AWS
- Using Jenkins to implement Continuous Integration and Continuous Deployment
- Building pipelines
- Working with Ansible and CloudFormation to deploy clusters
- Building Kubernetes clusters
- Building Docker containers in pipelines

## Propose and Scope the Project

- For the Docker application I used an Nginx “Hello World, my name is Luka.” application.
- As a deployment type, I applied a blue/green deployment.
- I used Jenkins to manage Continuous Integration phases.

## Project walkthrough Steps

### Create on EC2 an Ubuntu Server

I used an Ubuntu v20, and referenced this tutorial for Jenkins installation: https://www.journaldev.com/33965/install-jenkins-on-ubuntu

#### Step1: Install Prerequisites

sudo apt update
sudo apt install openjdk-8-jdk

#### Step 2: Retrieve and add the GPG Public Keys

wget https://pkg.jenkins.io/debian/jenkins.io.key
sudo apt-key add jenkins.io.key

#### Step 3: Add the Jenkins Repository to the Sources List

Insert "deb https://pkg.jenkins.io/debian-stable binary/" in /etc/apt/sources.list

#### Step 4: Install Jenkins on Ubuntu

sudo apt update
sudo apt install jenkins

#### Step 5: Verify Jenkins Installation

sudo systemctl status jenkins

#### Step 6: Allow incoming connections into Jenkins

sudo ufw allow 8080

#### Step 7: Visit the Jenkins Server on the Browser

http://ec2-3-15-154-201.us-east-2.compute.amazonaws.com:8080
