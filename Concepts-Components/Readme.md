## Providers
- Expose resources for specific infrastructure platform (aws)
- Responsible for understanding the api of the platform (aws)
  
Official providers are owned and maintained by Hashicorp

Verified providers are actively maintained and verified through Hashicorp, but owned by third parties.

Community providers - created by the community for others to use

Terraform init will install the providers we have defined and create a .lock.hcl file to lock the current version


## AWS

By default in AWS every region will have a VPC because your components (EC2, etc) need a VPC in order to run.

VPC is your own isolated network in the cloud.

Availability Zone = one or more discrete data centres.

A region can have multiple AZ's.

Your VPC will span all AZ's (subnets) in that region.

VPC is a virtual representation of network infrastructure.

Subnets span individual availability zones. Subnets are like a private network inside a network (VPC) with a sub range of IP addresses.

VPC has a range of private/internal IP addresses (IPv4 CIDR). This is not for outside web traffic, but for communication within the VPC.

To allow internet connectivity from your VPC, you need an Internet Gateway.

Firewall controls are available. By default the VPC is private and closed off to the world. Network ACLs (NACL) (firewall rules per subnet) and security groups (instance level) can be used for security.

In AWS, a network ACL (or NACL) controls traffic to or from a subnet according to a set of inbound and outbound rules. This means it represents network level security. For example, an inbound rule might deny incoming traffic from a range of IP addresses, while an outbound rule might allow all traffic to leave the subnet.

Because NACLs function at the subnet level of a VPC, each NACL can be applied to one or more subnets, but each subnet is required to be associated with one—and only one—NACL.

https://www.fugue.co/blog/cloud-network-security-101-aws-security-groups-vs-nacls
