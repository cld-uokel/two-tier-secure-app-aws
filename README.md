# Two-Tier Secure App — AWS

Follow-up to my first AWS project, where I built a VPC with public and private subnets,
EC2 instances in each, a route table to direct traffic, a security group to control 
communication between subnets, and an internet gateway to give the public subnet 
internet access.

This project builds on that foundation to create a secure two-tier web app: a web server 
on the public subnet and a database on the private subnet. I also plan to use Wireshark 
to capture and analyse traffic as I study for my CCNA certification.

## Goals
- Host a web server on the public subnet
- Host a database on the private subnet
- Use a NAT Gateway for outbound-only internet access from the private subnet
- Implement NACLs for layered network security
- Assign an Elastic IP for a stable public address (If my wallet permits)

## New concepts to learn
- NACLs
- NAT Gateway
- Elastic IPs
- VPC Flow Logs
