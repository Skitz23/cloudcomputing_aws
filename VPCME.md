# Virtual Private Cloud(VPC)

# what is vpc?
VPC stands for Virtual Private Cloud. It is a service offered by cloud computing providers, such as Amazon Web Services (AWS), Google Cloud Platform, and Microsoft Azure, that allows users to create a private network in the cloud.A VPC allows you to create and control a logically isolated section of the public cloud, which can be customized with your own private IP address range, subnets, route tables, and network gateways.

![](/pictures/VPC.png)

# How does vpc help the business?
VPCs can be very beneficial to businesses in several ways:
- Increased Security: By using a VPC, businesses can create a private, isolated network that is only accessible to authorized users and resources. This can help to prevent unauthorized access and can reduce the risk of security breaches.
- Scalability: VPCs allow businesses to scale their resources easily by creating additional virtual machines or instances in response to increased demand. This can help businesses to avoid over-provisioning, which can be costly, and can ensure that they have the necessary resources to handle spikes in traffic.
- Cost-Effective: VPCs can help businesses to reduce costs by eliminating the need to maintain and manage their own physical infrastructure. They also allow businesses to pay for only the resources they use, which can be more cost-effective than purchasing and maintaining their own hardware.
- Flexibility: VPCs allow businesses to customize their network configurations to meet their specific needs. This can include setting up their own IP address range, creating subnets, and configuring routing tables. This level of flexibility can help businesses to tailor their network infrastructure to their specific requirements.
- Hybrid Cloud: VPCs can enable businesses to connect their on-premises infrastructure with cloud resources.

# How does vpc help devops
VPCs can be very helpful for DevOps teams in many ways:
- Isolation: DevOps teams can use VPCs to create isolated development, testing, and production environments. This can help to prevent changes made in one environment from impacting others, and can also provide a secure environment for testing and development.
- Automation: VPCs can be easily configured and managed using infrastructure as code tools like Terraform, CloudFormation, and Ansible. This allows DevOps teams to easily provision and manage VPC resources 
- Security: VPCs allow DevOps teams to define their own network security groups, access control lists (ACLs), and firewall rules. This can then reduce the risk of security breach

# Why did AWS need to introduce a VPC virtual private cloud
AWS introduced the VPC (Virtual Private Cloud) service to provide customers with a way to create a private network environment in the AWS cloud.AWS customers had to use public IP addresses to connect their cloud resources to the internet, which made their infrastructure vulnerable to attacks from the public internet

# what is subnets
A subnet, short for subnetwork, is a smaller network within a larger network. It is created by dividing a larger network into smaller, more manageable sections to improve performance, security, and organization.In a subnet, all devices have IP addresses that are within a certain range, and communication is generally restricted to devices within that range.

A public subnet is a subnet within a network that is publicly accessible from the Internet. Devices within a public subnet have public IP addresses that can be reached from anywhere on the Internet. This makes public subnets ideal for hosting web servers, email servers, and other services that need to be publicly accessible.

A private subnet is a subnet within a network that is not publicly accessible from the Internet. Devices within a private subnet typically have private IP addresses, which are not routable on the Internet. To access devices within a private subnet, users must first connect to a device that is accessible from the Internet, such as a firewall or VPN gateway, and then connect to the private subnet over a secure connection. 

# CIDR
CIDR (Classless Inter-Domain Routing) is a method of allocating IP addresses and routing Internet Protocol (IP) packets. In CIDR, IP addresses are divided into variable-length "prefixes", which are denoted by a slash ("/") followed by a number indicating the length of the prefix.

CIDR blocks are ranges of IP addresses that are defined using CIDR notation. For example, the CIDR block 192.168.0.0/16 represents all IP addresses from 192.168.0.0 to 192.168.255.255, while the CIDR block 10.0.0.0/8 represents all IP addresses from 10.0.0.0 to 10.255.255.255.

CIDR blocks are used for subnetting, where a larger IP address range is divided into smaller subnets. Each subnet is assigned its own CIDR block, which determines the range of IP addresses that can be used by devices within that subnet.

# Internet gateway
An Internet gateway is a network component that provides connectivity between a local network and the Internet. It allows devices within the local network to access resources on the Internet, and enables communication between devices on the local network and devices on other networks.Internet gateway is a router that connects the local network to the Internet via an Internet service provider (ISP). The router is configured with a public IP address on its WAN (wide area network) interface, which allows it to communicate with devices on the Internet.

# Route table
A route table is a database that contains information about the networks and addresses that a router can reach, and how it can reach them. The route table is used by the router to determine the best path for forwarding packets between different networks.


# How to create a VPC
- Log in to your AWS account.
- Go to the AWS Management Console and select the region where you want to create the VPC.
- From the Services menu, select VPC.
- Click on "Your VPCs" and then click on "Create VPC".

Input the following

![](/pictures/CreateVPC.png)

# How to Create a Subnet
- Log in to your AWS account.
- Go to the AWS Management Console and select the region where your VPC is located.
- From the Services menu, select VPC.
- Click on "Subnets" and then click on "Create subnet".

Input the following

![](/pictures/VPCSubnet.png)

