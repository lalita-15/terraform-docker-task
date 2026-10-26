Infrastructure as Code (IaC) with Terraform



Internship Task 3 | Terraform + Docker



Objective

To create and manage a local Docker container using Terraform.



Tools I Used

\- Terraform

\- Docker Desktop

\- Nginx



Task Description

This project demonstrates how to provision a Docker container using Terraform. Terraform downloads the Nginx image and creates a container with port mapping.



\## Architecture



```mermaid

flowchart TD

&#x20;   A\["main.tf<br/>Terraform Configuration"] --> B\["terraform init"]

&#x20;   B --> C\["terraform plan"]

&#x20;   C --> D\["terraform apply"]

&#x20;   D --> E\["Docker Provider"]

&#x20;   E --> F\["Nginx Image<br/>nginx:latest"]

&#x20;   F --> G\["Docker Container<br/>terraform-nginx"]

&#x20;   G --> H\["Port Mapping<br/>localhost:8081 → 80"]

&#x20;   H --> I\["Nginx Welcome Page"]



&#x20;   J\["terraform state list"] -.-> G

&#x20;   K\["terraform destroy"] -.-> G



&#x20;   style A fill:#e8eaf6,stroke:#3949ab,color:#111

&#x20;   style D fill:#e8f5e9,stroke:#2e7d32,color:#111

&#x20;   style G fill:#e3f2fd,stroke:#1565c0,color:#111

&#x20;   style I fill:#fff3e0,stroke:#ef6c00,color:#111

```

Main Files

\- main.tf – Terraform configuration to create the Docker image and container.

\- execution-logs.txt – Commands and execution results.

\- screenshots – Screenshots showing successful execution proof.



Steps I followed to Perform Task:-



1\. Installed Terraform and verified Docker.

2\. Created the Terraform configuration in main.tf.

3\. Initialized Terraform using terraform init.

4\. Reviewed infrastructure changes using terraform plan.

5\. Syntax checked using terraform validate

6. Created the Docker container using terraform apply.
7. Verified resources using terraform state list.
8. Tested the Nginx application on http://localhost:8081.
9. Removed the resources using terraform destroy.



Expected Output:

A Docker container named terraform-nginx-container runs Nginx and exposes it on port 8080 of the local machine.

Apply complete! Resources: 2 added, 0 changed, 0 destroyed.



Verify Container

&#x20;docker ps



\## Cleanup

Run the following command to remove the Terraform-managed resources:



terraform destroy





Author

Lalita Rajpoot



Project: Internship Task 3 — Infrastructure as Code (IaC) with Terraform

