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



# Tier 2 architecture - Deploying our database VM on EC2

### Step 1
We need to SSH into our we do this by using the code from instance on AWS

```
ssh -i "devops-tech201.pem" ubuntu@ec2-3-252-164-141.eu-west-1.compute.amazonaws.com
```

### Step 2
We have to migrate the database provision.sh script we do this by typing
```
git clone + URL from the repository
```
The url from repositry is found on github

### Step 3
Navigate to the correct folder once thats done
```
sudo ./provision.sh
```
This code will allow us to run the file

### Step 4
Use the following code to change the permissions of the file
```
chmod 700 provision.sh
```
Once thats done type
```
 sudo systemctl restart mongod 
 sudo systemctl enable mongod
 sudo systemctl status mongod
 ```

 # Step 5
 Chnage the BindIP to 0.0.0.0 to be public
 To check the changes saved type
  ```
  cat mongod.conf
  ```

  # Step 6
  Naviagte to the app folder and type
  ```
  export DB_HOST=mongodb://db_instance_IP/posts
  ```
  Now type the following commands
  ```
  npm install
  npm start
  node seeds/seed.sj
  ```

  if the following steps are done correctly then go on AWS and get the ipaddress and type it on google for example
  ```
  http://54.229.41.99:3000/posts
  ```
  And the page should load

  ![](/postpage.png)