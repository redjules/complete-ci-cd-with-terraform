# Project description:
Integrate provisioning stage into complete CI/CD Pipeline to automate provisioning  server instead of deploying to an existing server
-	Create a SSH Key Pair
I created a server with Digital Ocean with a password and I ssh the ip with root:

![Screenshot 2024-10-28 at 18 16 36](https://github.com/user-attachments/assets/58887607-9b3b-4581-b96b-ba32acb3de83)

![Screenshot 2024-10-26 at 23 21 49](https://github.com/user-attachments/assets/b7cd4f7e-2172-4397-9911-d1c0c4f1fca8)

to not use a password, we will use SSH: 

![Screenshot 2024-10-26 at 23 20 11](https://github.com/user-attachments/assets/336db8c4-4ff0-417c-9f9b-e6b857624da0)

We open a new terminal:

![Screenshot 2024-10-28 at 18 31 23](https://github.com/user-attachments/assets/a1a52dcf-7340-4c4f-84b6-c4866397a2cf)

id_rsa is the private key and id_rsa.pub is the public key. The file where we add the public key of all the computers, all the client computers that want to connect to this server is the authorited_keys file:

![Screenshot 2024-10-26 at 23 20 40](https://github.com/user-attachments/assets/4c551bb6-7d5a-4e9b-8f10-6bdc5fa00c52)

<img width="635" alt="Screenshot 2024-10-28 at 18 35 36" src="https://github.com/user-attachments/assets/bb665ec5-e82a-4210-82b6-fbd6ffd94141">

now when we connect to the server it does ask for a password!:$

<img width="542" alt="Screenshot 2024-10-28 at 18 36 20" src="https://github.com/user-attachments/assets/ed7e6cbf-cd0c-4837-b74e-d56cd1311b93">

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
