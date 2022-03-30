# AWS Assignement 

### Problem Statement

Task

Create 1 VPC
eg : ninja-vpc-01

Create 1 IGW
eg : ninja-igw-01

Create 1 NAT
eg : ninja-nat-01

Create 2 Subnet
1 public subnet
eg : ninja-pub-sub-01


1 private subnet
eg : ninja-priv-sub-01

Create 2 Route Table

1 for public subnet
eg : ninja-route-pub-01


1 for private subnet
eg : ninja-route-priv-01


Create 2 ec2-instance

1 in public subnet
prefered ami : ubuntu
eg : ninja-ec2-pub-01

1 in private subnet
prefered ami : ubuntu
eg : ninja-ec2-priv-01

Ping ninja-ec2-priv-01  from ninja-ec2-pub-01  and vice-versa


## Assignment Solution
#### Step1 -- Select Region and Create VPC then define Ipv4 CIDR Range
![ Alt](https://github.com/coderpro2000/AWS/blob/main/images/vpc1.png)

#### Step 2 -- Create two subnet one is public and private subnet attach with given vpc and define CIDR range according to VPC CIDR
#### Public Subnet
![ Alt](https://github.com/coderpro2000/AWS/blob/main/images/vpc2.png)

#### Private Subnet
![ Alt](https://github.com/coderpro2000/AWS/blob/main/images/vpc3.png)

#### Step 3-- Define Route table for public and private subnets
Public subnet connect with public route
![ Alt](https://github.com/coderpro2000/AWS/blob/main/images/vpc4.png)

Private Subnet connect with private route
![ Alt](https://github.com/coderpro2000/AWS/blob/main/images/vpc5.png)

#### Step4 -- Create internet gateway and attach with vpc
![ Alt](https://github.com/coderpro2000/AWS/blob/main/images/vpc6.png)

#### Step5 -- This internet gateway connect with public route
![ Alt](https://github.com/coderpro2000/AWS/blob/main/images/vpc8.png)


#### Step6 -- Create NAT for private route and connect with private route
![ Alt](https://github.com/coderpro2000/AWS/blob/main/images/vpc7.png)
![ Alt](https://github.com/coderpro2000/AWS/blob/main/images/vpc9.png)

#### Step7 -- Crate two instance one is private and other is public
In public Instance Enable Public Ip and aatch with given VPC
![ Alt](https://github.com/coderpro2000/AWS/blob/main/images/vpc10.png)

In Private Instance Disable Public Ip and attach with given VPC
![ Alt](https://github.com/coderpro2000/AWS/blob/main/images/vpc11.png)

#### -- Step8 Create a Pem key and take a read permission in your terminal and connect with public instance via ssh
![ Alt](https://github.com/coderpro2000/AWS/blob/main/images/vpc12.png)

#### Step9-- Private instance call via public instance and ping internet service
![ Alt](https://github.com/coderpro2000/AWS/blob/main/images/vpc13.png)




