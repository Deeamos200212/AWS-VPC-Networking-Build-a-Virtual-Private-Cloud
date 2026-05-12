# AWS-VPC-Networking-Build-a-Virtual-Private-Cloud
AWS VPC Networking / Build a Virtual Private Cloud A hands‑on project that builds a custom AWS VPC from scratch. Includes VPC creation, subnet design, routing, and internet access configuration. Perfect for learning AWS networking fundamentals and preparing for real‑world cloud deployments.
<img width="379" height="29" alt="image" src="https://github.com/user-attachments/assets/56950c99-b6a1-4fc6-a7a1-6123dea17956" />

Overview
This project provisions a custom Amazon VPC (10.0.0.0/16) containing a public subnet (10.0.1.0/24) and a private subnet (10.0.2.0/24), each in a separate Availability Zone. An Internet Gateway (legendary-igw) is created and attached to enable outbound internet access from the public subnet. All resources were configured manually via the AWS Management Console in us-east-1 (N. Virginia) — no automation or IaC tooling used.

<img width="571" height="269" alt="image" src="https://github.com/user-attachments/assets/b271fa37-717a-49d6-81dd-d9f07b2fdbbb" />

<img width="568" height="339" alt="image" src="https://github.com/user-attachments/assets/a67f164d-3b3d-4679-8949-add9efc9324b" />

<img width="549" height="301" alt="image" src="https://github.com/user-attachments/assets/55ce7d4c-e49f-4bcb-9653-7908ff92ab86" />

Setup Summary
1.Create VPC legendary-aws-vpc with CIDR 10.0.0.0/16
2.Create Public Subnet (10.0.1.0/24, us-east-1a) and Private Subnet (10.0.2.0/24, us-east-1b)
3.Enable auto-assign public IPv4 on Public Subnet
4.Create Internet Gateway legendary-igw and attach to legendary-aws-vpc
5.Create route table public-rt — add route 0.0.0.0/0 → legendary-igw, associate with Public Subnet
6.Verify Private Subnet uses main route table (local traffic only — no IGW route

Next Steps
*Add a NAT Gateway in the public subnet for private subnet outbound internet access

*Configure Security Groups & NACLs for layered access control

*Enable VPC Flow Logs for traffic monitoring and auditing

*Launch EC2 instances in both subnets and test connectivity

*Explore VPC Peering or AWS Transit Gateway for multi-VPC networking
Resources

*Amazon VPC User Guide — AWS Documentation covering VPC concepts, subnets, IGWs, and route tables (AWS Docs → Amazon VPC)

*AWS Well-Architected Framework — Networking & Content Delivery — Best practices for secure, resilient network design on AWS

*RRFC 1918 — Address Allocation for Private Internets — Defines the private IP ranges used in this project (IETF Datatracker)

*RFC 4632 — Classless Inter-domain Routing (CIDR) — The specification underlying all CIDR notation and subnet math (IETF Datatracker)
AWS
