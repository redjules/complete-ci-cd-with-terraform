# Project description:
Integrate provisioning stage into complete CI/CD Pipeline to automate provisioning  server instead of deploying to an existing server
-	Create a SSH Key Pair
I created a server with Digital Ocean with a password and I ssh the ip with root:

![Screenshot 2024-10-26 at 23 21 49](https://github.com/user-attachments/assets/b7cd4f7e-2172-4397-9911-d1c0c4f1fca8)

![Screenshot 2024-10-26 at 23 20 11](https://github.com/user-attachments/assets/336db8c4-4ff0-417c-9f9b-e6b857624da0)

id_rsa is the privtae key and id_rsa.pub is the public key:

![Screenshot 2024-10-26 at 23 20 40](https://github.com/user-attachments/assets/4c551bb6-7d5a-4e9b-8f10-6bdc5fa00c52)


![Screenshot 2024-10-26 at 23 29 56](https://github.com/user-attachments/assets/d42e6a2f-cf0f-49df-a387-e840eee1b35f)

-	Install Terraform inside Jenkins container
-	Add Terraform configuration to application’s git repository
-	Adjust Jenkinsfile to add ‘provision’ step to the CI/CD pipeline that provisions EC2 instance
-	So the complete CI/CD project we build has the following configuration:
a.	CI step: build artifact for Java Maven application
b.	CI step: Build and push Docker image to Docker Hub
c.	CD step: Automatically provision EC2 instance using TF
d.	CD step: Deploy new application version on the provisioned EC2 instance with Docker Compose

# Create a SSH Key Pair

# Install Terraform inside Jenkins container

# Adjust Jenkinsfile to add ‘provision’ step to the CI/CD pipeline that provisions EC2 instance


# So the complete CI/CD project we build has the following configuration:
# a.	CI step: build artifact for Java Maven application
# b.	CI step: Build and push Docker image to Docker Hub
# c.	CD step: Automatically provision EC2 instance using TF
# d.	CD step: Deploy new application version on the provisioned EC2 instance with Docker Compose
