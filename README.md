## &#x20;   Infrastructure as Code (IaC) with Terraform



## &#x20;      *Internship Task 3 | Terraform + Docker*



### \## **Objective**

To create and manage a local Docker container using Terraform.



#### Tools I Used

\- Terraform

\- Docker Desktop

\- Nginx



#### Task Description

This project demonstrates how to provision a Docker container using Terraform. Terraform downloads the Nginx image and creates a container with port mapping.



#### &#x20;Workflow



```mermaid

flowchart TD

&#x20;   A\[main.tf] --> B\[terraform init]

&#x20;   B --> C\[terraform plan]

&#x20;   C --> D\[terraform apply]

&#x20;   D --> E\[Docker Container Created]

&#x20;   E --> F\[Verify Nginx on localhost:8081]

&#x20;   F --> G\[terraform state list]

&#x20;   G --> H\[terraform destroy]

```

#### Main Files

\- main.tf – Terraform configuration to create the Docker image and container.

\- execution-logs.txt – Commands and execution results.

\- screenshots – Screenshots showing successful execution proof.



#### Steps I followed to Perform Task:-

#### 

1\. Installed Terraform and verified Docker.

2\. Created the Terraform configuration in main.tf.

3\. Initialized Terraform using terraform init.

4\. Reviewed infrastructure changes using terraform plan.

5\. Syntax checked using terraform validate

6. Created the Docker container using terraform apply.
7. Verified resources using terraform state list.
8. Tested the Nginx application on http://localhost:8081.
9. Removed the resources using terraform destroy.



##### Expected Output:

A Docker container named terraform-nginx-container runs Nginx and exposes it on port 8080 of the local machine.

Apply complete! Resources: 2 added, 0 changed, 0 destroyed.



##### Verify Container

&#x20;docker ps



#### &#x20;Cleanup

Run the following command to remove the Terraform-managed resources:



terraform destroy





##### Author

Lalita Rajpoot



Project: Internship Task 3 — Infrastructure as Code (IaC) with Terraform

