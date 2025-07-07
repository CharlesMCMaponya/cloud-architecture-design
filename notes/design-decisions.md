# 📝 Design Decisions

## VPC

- Chose custom VPC to isolate the environment and have control over CIDR range.

## Subnets

- One public subnet (for Load Balancer + NAT)
- One or more private subnets (for EC2 + RDS)

## Security

- Restricted access using Security Groups.
- NAT Gateway allows private subnets to access internet securely.

## Application Tier

- React frontend on S3 + CloudFront for performance
- EC2 with Auto Scaling Group to handle load dynamically

## Database Tier

- RDS MySQL in Multi-AZ for high availability
