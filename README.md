# Read More

### Terraform-based project to create a VPC, Security Group, and EKS cluster:

## Overview

This repository contains Terraform code to automate the creation of an Amazon Web Services (AWS) infrastructure. It includes the configuration to set up a Virtual Private Cloud (VPC), a Security Group, and an Elastic Kubernetes Service (EKS) cluster within the VPC. The following sections will guide you through understanding and applying the Terraform configurations.

## Prerequisites

- AWS CLI installed and configured with appropriate IAM permissions.
- Terraform installed on your local machine.
- Basic understanding of AWS services like VPC, Security Groups, and EKS.

## Terraform Configuration

### 1. VPC Creation

The `vpc.tf` file defines the VPC resource along with associated subnets and route tables. This VPC will serve as the network boundary for our EKS cluster. The configuration includes:

- A CIDR block for the VPC.
- Public and private subnets.
- Route tables and internet gateway.

### 2. Security Group

The `security-group.tf` file configures a Security Group with rules to allow traffic to and from the EKS cluster. The security group settings include:

- Ingress and egress rules for necessary ports.
- Association with the VPC created in the previous step.

### 3. EKS Cluster

The `eks.tf` file contains the configuration to create an EKS cluster within the VPC. It includes:

- EKS cluster resource definition.
- Node group settings for worker nodes.
- IAM roles and policies required for EKS operations.

## Applying the Configuration

1. **Initialize Terraform**

   Run the following command to initialize Terraform and download necessary provider plugins:

   ```bash
   terraform init
   terraform plan
   terraform apply

## Verify Deployment

- Check the AWS Management Console to verify that the VPC, Security Group, and EKS cluster have been created successfully.

## Additional Notes

    - Ensure that your AWS credentials have the necessary permissions to create and manage the resources defined.
    - You can customize the Terraform files to suit your specific requirements, such as changing CIDR blocks or adjusting security group rules.
    - For more details on each Terraform resource, refer to the Terraform AWS Provider Documentation.

 ### All processes will take 20 minutes.


