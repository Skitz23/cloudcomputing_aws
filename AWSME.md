# What is 2 tier architecture in AWS?
The Two tier architecture consists of two layers which are the Client Tier and Database. In the two tier the application logic is either buried inside the user interface on the client or within the database on the server 

# Why do we need to make a 2-tier architecture?
By using a two-tiered architecture, end users do not have to remember the physical name of hosts that their messaging and calendar applications connect to. The Access-Layer Application hosts provide proxies to connect end users to their assigned messaging or calendar data center host.

![](/two%20tier.png)

# Virtual Private Cloud (VPC)
A virtual private cloud (VPC) is a secure, isolated private cloud hosted within a public cloud. VPC customers can run code, store data, host websites, and do anything else they could do in an ordinary private cloud, but the private cloud is hosted remotely by a public cloud provider.

# SSH Key pairs
Each SSH key pair includes two keys which are
- A public key that is copied to the SSH server and anyone with a copy of the public key can encrypt data and read the persons corresponding private key.
- A private key that remains with the user.
