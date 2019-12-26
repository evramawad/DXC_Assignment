# DXC Assignment

- VPC.yaml: 
Creates 2 public subnets, 3 private subnets, route tables, IGW and NAT instance deployed in public subnet 1 and allow resources in private subnets to access internet.

- Users.yaml: 
Creates Dev user which able to start/stop EC2s and RDSs & Test user which able to read on EC2s, RDSs console.

- Bastion.yaml: 
Creates 1 bastion host deployed in public subnet 1 and its security group with only one opened port is: 19991

- Tomcat-ALB.yaml: 
Creates ALB deployed in public subnet 1 & 2 and forward traffic to tomcat instance in private subnet 1 on port 8080 and there is cloudwatch alarm which reboot the instance in case of health check error.
Tomcat URL: http://tomca-elast-1fhmwpnqp8yh1-1583348721.us-west-2.elb.amazonaws.com/

- Jenkins-ALB.yaml: 
Creates ALB deployed in public subnet 1 & 2 and forward traffic to jenkins instance (deployed on tomcat) in private subnet 2 on port 8080 and there is cloudwatch alarm which reboot the instance in case of health check error.
Jenkins URL: http://jenki-elast-js9wxy2get8m-28712356.us-west-2.elb.amazonaws.com/jenkins

- RDS.yaml: 
Creates RDS MySql database in private subnet 3.

- Automatic start/stop EC2s & RDSs on scheduler using Lambda function. 
https://github.com/awslabs/aws-instance-scheduler

- Max security on pastion instance applied by just open SSH port which is 19991 and only from my network.
