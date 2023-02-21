# what is autoscaling?
Auto Scaling monitors your applications and automatically adjusts capacity to maintain steady, predictable performance at the lowest possible cost.The main components of AWS that are involved in autoscaling include autoscaling groups, Amazon Machine Image (AMI), load balancer, snapshot, and EC2 instance.

# Types of AWS autoscaling
There are four main types of AWS autoscaling:
- Manual scaling is when the number of instances can be increased or decreased manually using a CLI or console. 
- Scheduled scaling involves the automatic execution of scaling actions based on certain schedules. They can be executed at a specific time during the day, month, week, or year. 
- Dynamic scaling is the number of EC2 instances is changed automatically based on signals that are provided by a CloudWatch alarm. 
- Predictive scaling involves using machine learning algorithms to program the desired number of instances.

# Autoscaling group
An autoscaling group performs the following tasks:
- It adds or removes instances depending on the load of the server. When there is a high load, it will add instances. If the load is low, it will remove instances.
- It scales EC2 instances up or down, which helps in managing the availability of applications.
- It runs the required number of instances. For example, if the required number of instances is 5, then it will run 5 EC2 instances.

![](/pictures/Autoscaling.png)

# Benefits of autoscaling
- Sstup scaling quickly 
