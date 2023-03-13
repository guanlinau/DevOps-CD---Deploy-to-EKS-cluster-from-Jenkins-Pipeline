### CD - Deploy to EKS cluster from Jenkins Pipeline

### Technologies Used:

Kubernetes, Jenkins, AWS EKS, Docker, Linux

### Project Description:

1- Install kubectl and aws-iam-authenticator on a Jenkins server

2- Create kubeconfig file to connect to EKS cluster and add it on Jenkins server

3- Add AWS credentials on Jenkins for AWS account authentication

4- Extend and adjust Jenkinsfile of the previous CI/CD pipeline to configure connection to EKS cluster

### Instructions

###### Step 1: Create a eks cluster with nodegroup in aws

###### Step 2: Create and run jenkins server as container in created digitalocean droplet server

###### Step 3: Install kubectl and aws-iam-authenticator on jenkins server

1- Install kubectl as curl

2- Install aws-iam-authenticator as curl

###### Step 4: Create a config file for kubectl on jenkins server

```
vim config
```

![image](./images/Screenshot%202023-03-13%20at%208.20.43%20pm.png)
![image](./images/Screenshot%202023-03-13%20at%208.39.33%20pm.png)

###### Step 5: Add AWS credentials on Jenkins for AWS account authentication

1-Create a jenkins-user on aws and save its access_id and secret_key

2-Create aws credentials on Jenkins with aws jenkins-user's access_id and secret_key
![image](./images/Screenshot%202023-03-13%20at%209.24.53%20pm.png)
![image](./images/Screenshot%202023-03-13%20at%209.25.26%20pm.png)

###### Step 6: Add deploy step in Jenkinsfile of the previous CI/CD pipeline to configure connection to EKS cluster

![image](./images/Screenshot%202023-03-13%20at%2011.26.58%20pm.png)
