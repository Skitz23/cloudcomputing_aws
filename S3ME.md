# S3 (Simple storage service)

# What is S3?
S3 stands for Simple Storage Service which is a cloud-based storage service provided by AWS. It is designed for storing and retrieving any amount of data from anywhere on the internet.S3 is highly scalable and can store and retrieve any amount of data, ranging from a few gigabytes to several terabytes or even petabytes.

# Why should we use S3 and its benefits?
Their are many reasons why we should use s3:
- Scalability: S3 is designed to handle any amount of data and can scale up or down as per the changing storage requirements of an organization.
- Durability: S3 is highly durable this means that the data stored in S3 is replicated across multiple devices and multiple availability zones providing high availability and protection against data loss.
- Security: S3 provides robust security features such as encryption, access control, and logging, to ensure that data is stored securely and accessed only by authorized users.
- Cost-effective: S3 offers a cost-effective storage solution compared to traditional storage systems, as users only pay for the amount of storage they use.
- Easy management: S3 offers easy-to-use management features, allowing users to create, store, and manage their data with ease.
- Integrations: Amazon S3 can integrate with other AWS services, making it easy to build applications that require cloud storage. It can also integrate with third-party tools.

# Disaster recovery
Amazon S3 is a popular service for disaster recovery as it provides high durability, availability, and security for storing and retrieving data, making it a reliable platform for disaster recovery. Furthermore, S3 provides built-in replication capabilities, allowing you to replicate data across regions or within a region. This ensures that your data is available even in the event of a regional outage.

# social media storage
Amazon S3 can be used for storing social media data, including images, videos, and other multimedia content. Social media companies often have to deal with massive amounts of user-generated content, and S3 can provide a scalable and cost-effective solution for storing this data.


# CRUD (Create, Read, Update, and Delete)
These operations represent the basic functionalities that allow users to interact with databse or application.
- Create: This operation allows users to add new data to the system or database.
- Read: This operation allows users to retrieve data from the system or database.
- Update: This operation allows users to modify or update existing data in the system or database.
- Delete: This operation allows users to remove data from the system or database.

# How to create a AWS S3 Bucket?

### Step 1
SSH into your EC2 instance on gitbash terminal

### Step 2
Type the following command
```
sudo apt update -y
sudo apt upgrade -y
```

### Step 3
we need to install python to do this we type the following command
```
sudo apt install python -y
```

we then need to check the version on python so we type
```
python --version
```
If the python version is not 3.6.9 type the following command
```
alias python=python3
```
Now check the version again and it should say 3.6.9

### Step 4
Type the following command
```
sudo apt install python3-pip
sudo pip3 install awscli
```

### Step 5
Type the following command
```
aws configure
```
The terminal will ask you for the following
- AWS Access Key ID
- AWS Secret Access Key
- Default region name 
- Default output format

Now type the following code
```
aws s3 ls
```

### Step 6
This code will create a bucket
```
aws s3 mb s3://zain-tech201
```
### Step 7 
we need to make a text file and write a message in it so type the following command
```
sudo touch test.txt
sudo nano test.txt - Then type a message
```

Now type this code below
```
aws s3 cp test.txt s3://zain-tech201
```

### Step 8

Go to aws s3 buckets and enable the following settings on your textfile created
![](/pictures/s3.png)

Now copy the object url into google and the following page should appear
![](/pictures/s3webpage.png)

# S3 Diagram
![](/pictures/s3diagram.png)





