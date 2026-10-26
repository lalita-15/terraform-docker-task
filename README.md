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



Architecture



&#x20;       Terraform Configuration

&#x20;              main.tf

&#x20;                 |

&#x20;                 v

&#x20;          Terraform CLI

&#x20;                 |

&#x20;         +-------+-------+

&#x20;         |               |

&#x20;         v               v

&#x20;    Docker Image    Docker Container

&#x20;     nginx:latest   terraform-nginx-container

&#x20;                         |

&#x20;                         v

&#x20;                 Host Port: 8081

&#x20;                         |

&#x20;                         v

&#x20;                  Container Port: 80

&#x20;                         |

&#x20;                         v

&#x20;                   Nginx Web Page



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

