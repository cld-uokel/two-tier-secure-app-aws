# Architecture

## Current Architecture
- VPC: `10.0.0.0/16`
- Public subnet: `10.0.1.0/24`, hosts web server and NAT Gateway
- Private subnet: `10.0.2.0/24`, hosts database server
- Internet Gateway: allows public subnet to reach the internet
- NAT Gateway: allows private subnet outbound internet access only

## EC2 Instances
- `web-server`: public subnet, has public IP
- `database-server`: private subnet, no public IP