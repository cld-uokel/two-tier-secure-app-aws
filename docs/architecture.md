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

## Security
- `web-server-sg`: allows HTTP (80) and SSH (22) from anywhere
- `database-server-sg`: allows MySQL (3306) only from `web-server-sg`

### NACLs (Network ACLs)
- `public-nacl`: allows HTTP,HTTPs, SSH inbound;
- `private-nacl`: allows traffic from public subnet (10.0.1.0/24) only

## Web Server
- Installed Apache on`web-server` EC2 to serve a simple HTML page
- Accessible via public IP on port 80
