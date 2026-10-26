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



&#x20;    Architecture



```mermaid

flowchart TD

&#x20;   A\["main.tf<br/>Terraform Configuration"]

&#x20;   B\["terraform init"]

&#x20;   C\["terraform plan"]

&#x20;   D\["terraform apply"]

&#x20;   E\["Docker Provider"]

&#x20;   F\["Nginx Image"]

&#x20;   G\["Docker Container<br/>terraform-nginx"]

&#x20;   H\["localhost:8081"]

&#x20;   I\["Nginx Welcome Page"]



&#x20;   A --> B --> C --> D --> E

&#x20;   E --> F --> G --> H --> I



&#x20;   J\["terraform state list"] -.-> G

&#x20;   K\["terraform destroy"] -.-> G



&#x20;   classDef config fill:#dbeafe,stroke:#2563eb,color:#111827

&#x20;   classDef process fill:#f3f4f6,stroke:#6b7280,color:#111827

&#x20;   classDef resource fill:#dcfce7,stroke:#16a34a,color:#111827

&#x20;   classDef verify fill:#fef3c7,stroke:#d97706,color:#111827



&#x20;   class A config

&#x20;   class B,C,D,E process

&#x20;   class F,G resource

&#x20;   class H,I verify

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

