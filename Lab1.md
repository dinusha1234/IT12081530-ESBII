####NAME : K.D.D. Chathurangi

####REG.NO : IT12081530

####SUBJECT : ENTERPRISE STANDARDS AND BEST PRACTICES FOR IT INFRASTRUCTURE

####LAB : 01

#CREATING AN AMAZON EBS-BACKED WINDOWS AMI

###Launching an Instance

1.Open the Amazon EC2 console

![1](https://cloud.githubusercontent.com/assets/13193749/8743177/61638b62-2c8a-11e5-8e17-a0e7ef9a67ac.png)

2.In the navigation bar at the top of the screen, the current region is displayed. Select the region for the instance. 

3.From the Amazon EC2 console dashboard, click Launch Instance.

4.On the Choose an Amazon Machine Image (AMI) page, choose an AMI.

5.On the Choose an Instance Type page, select the hardware configuration and size of the instance to launch. Eligible for the free tier, select the t2.micro instance type. Note --> Set up an instance quickly for testing purposes, you can click Review and Launch at this point to accept default configuration settings, and launch your instance.

To configure your instance further, click Next: Configure Instance Details.

6.On the Configure Instance Details page, change the settings as necessary and then click Next. ( Here I have selected the default configuration settings )

7.On the Add Storage page, you can specify volumes to attach to the instance besides the volumes specified by the AMI (such as the root device volume) then click Next: Tag Instance when you have finished.

8.On the Configure Security Group page, use a security group to define firewall rules for your instance. These rules specify which incoming network traffic is delivered to your instance. All other traffic is ignored. Select or create a security group and then click Review and Launch.

Here I have selected create a new security group.

In Create a new security group the wizard automatically defines the launch-wizard-x security group.You can edit the name and description of the security group.

Here I have edited the name and the description as shown in the prints screen.

The wizard automatically defines an inbound rule to allow to you connect to your instance over SSH (port 22) for Linux or RDP (port 3389) for Windows.

9.On the Review Instance Launch page, check the details of your instance, and make any necessary changes by clicking the appropriate Edit link.When you are ready, click Launch.

10.In the Select an existing key pair or create a new key pair dialog box, you can choose an existing key pair, or create a new one. Here I have created a new key pair.

To launch your instance, select the acknowledgment check box, then click Launch Instances.

Note --> If you select the Proceed without key pair option, you won't be able to connect to the instance unless you choose an AMI that is configured to allow users another way to log in.

11.Launch Instance


### Connect Using Remote Desktop

1. Connect Using Remote Desktop

2. Logging to the remote desktop

3. Connecting to the virtual machine in cloud





