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

### Create on EC2 an Ubuntu Server (Screenshot 1 till Screenshot 9)

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

#### Step 6: Allow incoming connections into Jenkins and install tidy

sudo ufw allow 8080
sudo apt install tidy

### Created Jenkins pipeline

I created a Jenkinse pipeline. The result of the pipeline: Screenshot 11 - Jenkis pipeline
I pushed the created docker image on Docker Hub: Screenshot 10 - DockerHub Repository

### Code is checked against a linter as part of a Continuous Integration step (demonstrated w/ two screenshots)

Screenshot 11b - Lint

### The project performs the correct steps to do a blue/green or a rolling deployment into the environment selected. Student demonstrates the successful completion of chosen deployment methodology with screenshots.

Screenshot 12b - blue/green

Check Screenshot

### Test the website

I took the ip address from the Loadbalancer: Screenshot 12 - Load Balancer
I tested the Web App: Screenshot 13 - Test Web App

You can also test the app using this link:
http://a190749029db54eea98afcfbeb9c8974-1535868717.us-east-2.elb.amazonaws.com:8000
