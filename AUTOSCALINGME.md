# what is autoscaling?
Auto Scaling monitors your applications and automatically adjusts capacity to maintain steady, predictable performance at the lowest possible cost.The main components of AWS that are involved in autoscaling include autoscaling groups, Amazon Machine Image (AMI), load balancer, snapshot, and EC2 instance.

# Types of AWS autoscaling
There are four main types of AWS autoscaling:
- Manual scaling is when the number of instances can be increased or decreased manually using a CLI or console. 
- Scheduled scaling involves the automatic execution of scaling actions based on certain schedules. They can be executed at a specific time during the day, month, week, or year. 
- Dynamic scaling is the number of EC2 instances is changed automatically based on signals that are provided by a CloudWatch alarm. 
- Predictive scaling involves using machine learning algorithms to program the desired number of instances.

# Components of autoscaling

### Autoscaling group
An autoscaling group performs the following tasks:
- It adds or removes instances depending on the load of the server. When there is a high load, it will add instances. If the load is low, it will remove instances.
- It scales EC2 instances up or down, which helps in managing the availability of applications.
- It runs the required number of instances. For example, if the required number of instances is 5, then it will run 5 EC2 instances.

# Benefits of autoscaling
- Anticipate costs and avoid overspending: AWS Auto Scaling can help you optimize your utilization and cost efficiencies when consuming AWS services so you only pay for the resources you actually need. When demand drops, AWS Auto Scaling will automatically remove any excess resource capacity so you avoid overspending.
- Make smart scaling decisions: AWS Auto Scaling lets you automate how groups of different resources respond to changes in demand. Easy-to-understand scaling strategies let you choose to optimize availability, costs, or a balance of both.
- Predictable scaling : AWS Auto Scaling calculates the minimum and maximum limits between which your resources will scale. 

# How to Create a launch template

### Step 1 
Go on lauch template and create a template for the user data include the following code
```
#!/bin/bash
sudo apt update -y 
sudo apt upgrade -y

sudo apt install nginx -y 
sudo systemctl restart nginx
sudo systemctl enable nginx
```

# How to create a autoscaling group?

### Step 1
In the AWS Management Console, navigate to the EC2 service and click on "Auto Scaling Groups" in the left-hand menu.

### Step 2
Click on the "Create Auto Scaling group" button.

### Step3
Select your launch configuration, which you previously created.

### Step 4
Configure the autoscaling group settings, including the desired capacity, minimum and maximum capacity, subnets, load balancers, and health check settings.
For the desired capacity and minimum capacity i chose 2 but for the maximum capacity i chose 3

### Step 5
For the next Step I chose the following:

- Scaling policy name: Target Tracking Policy
- Metric type: Average CPU util
- Target value: 50%
- Instance need: 300 seconds before warm up

### Step 6
Review your settings and launch the autoscaling group.
After you have created your autoscaling group, you can use the AWS console to monitor its performance and adjust its settings as needed.

![](/pictures/Autoscaling.png)