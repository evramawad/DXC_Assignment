DXC Assignment

- VPC.yaml
Creates 2 public subnets, 3 private subnets, route tables, IGW and NAT instance deployed in public subnet 1 and allow resources in private subnets to access internet.

- Users.yaml
Creates Dev user which able to start/stop EC2s and RDSs & Test user which able to read on EC2s, RDSs console.

- Bastion.yaml
Creates 1 bastion host deployed in public subnet 1 and its security group with only one opened port is: 19991

- Tomcat-ALB.yaml
Creates ALB deployed in public subnet 1 & 2 and forward traffic to ec2 instance in private subnet 1 on port 8080 and there is cloudwatch alarm which reboot the instance in case of health check error.

- Jenkins-ALB.yaml
Creates ALB deployed in public subnet 1 & 2 and forward traffic to ec2 instance in private subnet 2 on port 9090 and there is cloudwatch alarm which reboot the instance in case of health check error.

- RDS.yaml
Creates MySql database in private subnet 3.
