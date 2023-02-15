# cloudcomputing_aws

# How to Step up AWS account

### Step 1

Once you recieve your login for AWS go to the website login and make sure you change the password

### Step 2

Go to the top right and change the region to Europe(Ireland)

![](/AWS.png)


# What is AWS?
AWS stands for Amazon Web Services and is a comprehensive, evolving cloud computing platform provided by Amazon that includes a mixture of infrastructure-as-a-service (IaaS), platform-as-a-service (PaaS) and packaged-software-as-a-service (SaaS) offerings. AWS services can offer an organization tools such as compute power, database storage and content delivery services.


# History of AWS?
In 2006, Amazon Web Services (AWS) began offering IT infrastructure services to businesses in the form of web services -- now commonly known as cloud computing. One of the key benefits of cloud computing is the opportunity to replace up-front capital infrastructure expenses with low variable costs that scale with your business. With the Cloud, businesses no longer need to plan for and procure servers and other IT infrastructure weeks or months in advance. Instead, they can instantly spin up hundreds or thousands of servers in minutes and deliver results faster.

# Who are some of the other leaders in Cloud technology?
Microsoft Azure was launched in 2010, offering more than 200 products and cloud services on its platform. Users can build, run, and manage applications across not only clouds but also on-premises, and at the edge. 95% of Fortune 500 companies trust their business with Azure.

Google Cloud includes a broad suite of services accessed over the internet that help organizations go digital. Google Cloud Platform (which provides public cloud infrastructure for web-based applications) is a part of the larger Google Cloud suite. Since it first came online in 2008, some notable customers include LinkedIn, NewsCorp, Facebook, Verizon, and Twitch.

Alibaba Group’s cloud computing unit, known as Alibaba Cloud, is the fourth largest cloud service provider globally, the primary cloud vendor in Asia Pacific, and the largest cloud service provider in China. Through Alibaba Cloud, the business offers cloud services, including elastic computing, database, storage, network virtualization, large-scale computing, security, management & application services, big data analytics, and machine learning.
Alibaba Cloud currently has 27 regions and 84 availability zones in operation


# what is cloud computing?
Cloud computing is the on demand delivery of IT resources over the Internet with pay-as-you-go pricing. Instead of buying, owning, and maintaining physical data centers and servers, you can access technology services, such as computing power, storage, and databases, on an as-needed basis from a cloud provider like Amazon Web Services.


# Benefits of cloud computing
Cloud computing has many benefits some of them are:
- Agility this gives you easy access to a broad range of technologies so that you can innovate faster and build nearly anything that you can imagine.
- Cost savings this is when the cloud allows you to trade fixed expenses (such as data centers and physical servers) for variable expenses, and only pay for IT as you consume it.
- Deploy globally in minutes this means that you can expand to new geographic regions and deploy globally in minutes. For example, AWS has infrastructure all over the world, so you can deploy your application in multiple physical locations with just a few clicks.

# Types of Cloud Computing
- Infrastructure as a service (IaaS) is a type of cloud computing service that offers essential compute, storage, and networking resources on demand, on a pay-as-you-go basis. IaaS is one of the four types of cloud services

- Platform as a service (PaaS) is a cloud computing model where a third-party provider delivers hardware and software tools to users over the internet. Usually, these tools are needed for application development.

- Software as a service (or SaaS) is a way of delivering applications over the Internet—as a service. Instead of installing and maintaining software, you simply access it via the Internet, freeing yourself from complex software and hardware management.

# How to run AWS

Go on AWS and naviage to EC2 Dashboards once your their click instances(running) the page should look like the image below
![](/AWS%20Naviagte.png)

Once you click the instance running page click your instance and connect
![](/Screenshot_20230215_134222.png)

Run gitbash terminal and type 

```
Cd .ssh
sudo apt-get update -y 
sudo apt-get install nginx -y
chmod 400 devops-tech201.pem
ssh -i "devops-tech201.pem" ubuntu@ec2-52-215-79-130.eu-west-1.compute.amazonaws.com
```
once done type the ip address into google and you should have this page

![](/nginx.png)

# Diagram
![](/diagram.png)







