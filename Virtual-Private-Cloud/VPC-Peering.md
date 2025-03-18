**VPC-Peering**

![](Aspose.Words.c3c0436e-c58d-44f8-ad10-ca8ed2b299b8.001.png)

• Create VPC-A in Mumbai (ap-south-1) region (CIDR: 10.10.0.0/16)

• Create Internet Gateway and Attach to VPC-A

• Create Public Subnet in VPC-A (10.10.0.0/24)

• Launch EC2 instance and assign Public IP. Open inbound port 22 for your IP.

![](Aspose.Words.c3c0436e-c58d-44f8-ad10-ca8ed2b299b8.002.png)

• Create VPC-B in North Virginia (us-east-1) region (CIDR: 10.20.0.0/16)

• Create Private Subnet in VPC-B (10.20.0.0/24)

• Launch EC2 instance in the private subnet. Open inbound port 22 and ICMP for VPC-A CIDR range

![](Aspose.Words.c3c0436e-c58d-44f8-ad10-ca8ed2b299b8.003.png)

• Create a VPC peering connection request from VPC-A to VPC-B

VPC-A is the requestor and VPC-B is the acceptor.

• Accept the connection request in VPC-B

• Modify route tables on both sides for traffic on other VPC

![](Aspose.Words.c3c0436e-c58d-44f8-ad10-ca8ed2b299b8.004.png)

![](Aspose.Words.c3c0436e-c58d-44f8-ad10-ca8ed2b299b8.005.png)

• Login To the EC2-A instance and try to connect to EC2-B (ping or SSH) . Connect to the instance in VPC-B via SSH, and ping the instance EC2-A.

Note: Attach Internet Gateway to VPC and Route Tables to subnets.
