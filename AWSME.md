# What is 2 tier architecture in AWS?
The Two tier architecture consists of two layers which are the Client Tier and Database. In the two tier the application logic is either buried inside the user interface on the client or within the database on the server 

# Why do we need to make a 2-tier architecture?
By using a two-tiered architecture, end users do not have to remember the physical name of hosts that their messaging and calendar applications connect to. The Access-Layer Application hosts provide proxies to connect end users to their assigned messaging or calendar data center host.

![](/AWStech2diagram.png)

# Virtual Private Cloud (VPC)
A virtual private cloud (VPC) is a secure, isolated private cloud hosted within a public cloud. VPC customers can run code, store data, host websites, and do anything else they could do in an ordinary private cloud, but the private cloud is hosted remotely by a public cloud provider.

# SSH Key pairs
Each SSH key pair includes two keys which are
- A public key that is copied to the SSH server and anyone with a copy of the public key can encrypt data and read the persons corresponding private key.
- A private key that remains with the user.

# Requirements

- App tier deployed -> available on public IP
- Create 2nd tier with required dependencies: Ubuntu 18.04, mongodob installed, change mongod.conf 0.0.0.0.
- Need a security group for our database - allow 27017 from anywhere - allow only from app instance
- Go back to the app and create an environment variable with the database endpoint
- Relaunch the app

