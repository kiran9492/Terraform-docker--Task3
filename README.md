Terraform-Based Docker Container Provisioning

 Project Overview :
This project demonstrates how to **provision and manage a local Docker container using Terraform**.  
The infrastructure is defined using **Terraform configuration files** and executed through **Bash commands**, showcasing the concept of **Infrastructure as Code (IaC)**.

By using Terraform, Docker resources such as images and containers are created, managed, and destroyed in an automated and repeatable manner.

---

  Objective :
- Provision a **local Docker container** using Terraform
- Automate Docker image pulling and container creation
- Execute infrastructure provisioning using Bash commands
- Understand Terraform provider configuration and resource lifecycle

---

 🛠 Tools & Technologies
| Tool | Purpose |
|----|----|
| Terraform | Infrastructure provisioning |
| Docker | Container runtime |
| Bash | Command-line execution |
| Docker Hub | Image repository |

---

 Project Structure :
    terraform-docker/
    │
    ├── main.tf # Terraform configuration file
    └── README.md # Project documentation

Terraform Configuration Details :
The `main.tf` file includes:
- Terraform block to define required providers
- Docker provider configuration
- Docker image resource to pull the Nginx image
- Docker container resource with port mapping

Terraform automatically handles dependencies between resources, ensuring the Docker image is pulled before creating the container.

Prerequisites :
 Ensure the following are installed on your system:
   - Docker (Docker Desktop or Docker Engine)
   - Terraform
   - Bash-compatible terminal (Linux / macOS / Git Bash / WSL)

 Verify installations:
```bash
docker --version
terraform --version

Execution Steps:
 Step 1: Initialize Terraform
   Initializes the working directory and downloads required provider plugins.
  -terraform init

Step 2: Validate Configuration
  Checks the Terraform configuration for syntax and logical errors.
  -terraform validate

Step 3: Plan Infrastructure
  Displays a preview of resources Terraform will create.
  -terraform plan

Step 4: Apply Configuration
  Creates Docker image and container as defined in main.tf.
  -terraform apply

Step 5: Verify Docker Container
  Check running containers:
  -docker ps
Access the application in a browser:
   -Localhost:8080

Sample Execution Logs:
     Initializing provider plugins...
     Terraform has been successfully initialized!

     Plan: 2 to add, 0 to change, 0 to destroy.

     docker_image.nginx_image: Pulling image...
     docker_container.nginx_container: Creation complete

     Apply complete! Resources: 2 added, 0 changed, 0 destroyed.

Terraform Resource Lifecycle

Terraform manages infrastructure through the following lifecycle:

 1. Init – Provider initialization

 2. Plan – Execution preview

 3. Apply – Resource creation

 4. Destroy – Resource deletion

Outcome:

   1. Docker image successfully pulled from Docker Hub

   2. Docker container created and managed via Terraform

   3. Application exposed on local port

   4. Infrastructure automated using IaC principles

Useful Commands Reference :
   terraform init
   terraform validate
   terraform plan
   terraform apply
   terraform destroy
   docker ps



<img width="1366" height="768" alt="Task3 -1" src="https://github.com/user-attachments/assets/aa5f6e46-2796-4b70-998e-136a4ce57cc4" />




<img width="1366" height="768" alt="Task3 -2" src="https://github.com/user-attachments/assets/e109a6a0-bf93-43a4-9862-24eba49471c7" />




<img width="1366" height="768" alt="Task3-3" src="https://github.com/user-attachments/assets/1a03f90b-ca95-49a4-bb63-f402d37f9f4b" />




<img width="1366" height="768" alt="Task3-4" src="https://github.com/user-attachments/assets/a2a9e7b7-7ba7-4c69-9845-f47e34788ccb" />





<img width="1366" height="768" alt="Task3-5" src="https://github.com/user-attachments/assets/83a496d7-1ab1-4553-9c72-0453afa56c39" />
