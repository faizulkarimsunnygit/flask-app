
# Deploy of a 2 tier flask application on EKS with Jenkins CI-CD pipeline

This is a simple Flask app that interacts with a MySQL database. The app allows users to submit messages, which are then stored in the database and displayed on the frontend.

## Prerequisites
Docker
docker-compose 
AWS EC2 / VM machine 
EKS (Elastic Kubernetes Service)

## Installation
1. Docker ️🐋
2. docker-compose 
3. aws cli
4. eksctl 
5. unzip 
6. jenkins 🛠️🔧
7. kubectl ☸️ etc. 


    
## Deployment

1. SSH to the EC2 Instance
2. Install all required updates 
3. Install Jenkins and make the service enabled and up.
4. Install docker.io and make it accessable with user jenkins 
5. Git Clone the repository to the EC2 Machine 
6. Run the docker compose file by using "docker-compose up -d". it is present inside of the docker compose folder.
7. log in to the Jenkins. Make user for next time login. goto the pipeline section and add a job. put the trigger section and select "Github webhook". add the "jenkins url/github-webhook" into the github repo settings so that when any push happens trigger will be generated.
8. Go to the pipeline section and paste the code from the jenkinsfile to the pipeline section. you will find this on the repo. 
9. Create a IAM role and access token. 
10. install aws cli and configure it with token.
11. install eksctl took to create cluster on EKS.
12. run command eksctl with the desired node and node type.
13. run kubectl apply -f namespace.yaml to create the namespace.
14. run the pipeline. 
if everthing goes ok pipeline will build and deploy the pod to the EKS cluster. 

To Verify Kubernetes pod and Service 
command 
kubectl get nodes -n two-tier-ns 
kubectl get pods -n two-tier-ns -o wide 
kubectl get all -n two-tier-ns 

copy the EXTERNAL-IP from the flask app service and paste it on a browser. 


    


## Screenshots

Network Diagram of the Project 

Link -- https://ibb.co/0VXFpXw



## Documentation

[Documentation](https://faizulkarimsunny.atlassian.net/wiki/external/ZDhhYTY4ZTM3ZDk5NGZjY2E2NWZhNTEwYTMzNzMxYzM)


# Hi, I'm Faizul Karim! 👋



## 🚀 About Me
DevOps Engineer with a robust background in Linux, excelling in orchestrating Docker and Kubernetes environments both in local and Cloud. Specialized in AWS services such as ECS, EKS, and RDS, I ensure the seamless operation of microservices. Proficient in networking and troubleshooting, I contribute to the design and maintenance of scalable architectures. My expertise extends to implementing monitoring solutions with ELK Stack, Prometheus, Grafana, and AWS-native tools. Committed to continuous learning, I stay ahead in the dynamic DevOps landscape, leveraging emerging technologies for innovation.


## 🛠 Skills
Terraform, Kubernetes, Docker, Jenkins, Ansible, ECS, EKS, ELK, Grafana, Loki, Prometheus, cAdvisor || AWS, DO|| Red Hat Certified || RHCSA v7, RHCE v7 || RED HAT Virtualization, HA Clustering


## 🔗 Links
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](www.linkedin.com/in/faizulkarim/)



## Badges

Add badges from somewhere like: [shields.io](https://shields.io/)

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)
[![AGPL License](https://img.shields.io/badge/license-AGPL-blue.svg)](http://www.gnu.org/licenses/agpl-3.0)
