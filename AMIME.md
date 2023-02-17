# What is an AMI?
An AMI stands for Amazon Machine Image and is a pre-configured virtual machine image used to create and launch instances of EC2 instances in the cloud. An AMI includes the operating system, application server, and any additional software needed to run an application on an EC2 instance.

# How to create an AMI image

# Step 1
Once you created your app instance you have to select it and click actions and select image and templates and select create image.The image below is a guide on the step
![](/pictures/AMI.png)

# Step 2
Fill in the AMI name and description scroll down and select 8GB as the strorage and scroll down towards the right it should say create image.Once thats done the following page should appear.
![](/pictures/AMI2.png)

# Diagram
![](/pictures/AMIdiagram.png)


# How to run app AMI?

### Step 1
Create an Ami for database to do this follow the steps for how to create an AMI image but change the name to yourname-tech201-db-ami for example
![](/pictures/tech201-db.png)

Once thats created make another AMI for app and call it the same thing but change the name to yourname-tech201-db-ami

### Step 2
Once thats done coonect to the Databases AMI and copy the following highlighted code into gitbash terminal.Make sure to Cd into .ssh/ before you enter the database ami code
![](/pictures/amissh.png)

### Step 3
In the following code change the word "root" to "Ubuntu" and make sure to change the ipaddress as well to get you own ipaddress go on Ec2 instance connect 

![](/pictures/EC2ipaddress.png)

### Step 4
Install of the dependencies the code for that is
```
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv D68FA50FEA312927
echo "deb https://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.2.list
sudo apt-get update -y
sudo apt-get upgrade -y
sudo apt-get install -y mongodb-org=3.2.20 mongodb-org-server=3.2.20 mongodb-org-shell=3.2.20 mongodb-org-mongos=3.2.20 mongodb-org-tools=3.2.20
sudo systemctl start mongod
sudo systemctl enable mongod
```

### Step 4
Go on th gitbash terminal and type the following code with your ipaddress
```
export DB_HOST=mongodb://54.76.31.254/posts
printenv DB_HOST
Cd app
cd app
```

### Step 5
To lauch the post page type the following command
```
npm start
```

# How to set up an alarm for our EC2 app

### Step 1
Open the CloudWatch console (https://console.aws.amazon.com/cloudwatch/).
### Step 2
In the navigation pane, click "Alarms" and then click the "Create alarm" button.
### Step 3
In the "Select metric" section, click the "EC2 Metrics" tab.
### Step 4
In the "By Instance ID" section, select the EC2 instance that you want to set up an alarm for.
### Step 5
In the "Select metric" section, choose a metric to monitor, such as CPU utilization or network in/out.
### Step 6
Specify the conditions that will trigger the alarm. For example, you might want to set the threshold to 80% CPU utilization for 5 minutes.
### Step 7
Choose the actions to take when the alarm is triggered. You can choose to send a notification, such as an email or SMS message, or perform an action, such as stopping or terminating the instance.
### Step 8
Give the alarm a name and a description, and then click the "Create alarm" button.


