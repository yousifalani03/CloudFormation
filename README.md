# CloudFormation
I set up a Bastion Host in the Public Subnet of Availability Zone 1 to allow SSH access from my local machine to get through the Internet Gateway. Once connected to the Bastion Host, I SSH’d into the EC2 instance in the App Subnet In the first Availability Zone, which is a private subnet, while following the Security Group rules that permit traffic from the Bastion host.

After gaining access to that EC2 instance, I then pinged the EC2 instance in the Private Subnet of Availability Zone 2 through its private IP, which then allowed me to cross over to the second Availability Zone within the same VPC.

All the deployment from CloudFormation is in the vpc.yaml file.