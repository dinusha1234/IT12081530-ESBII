####NAME : K.D.D. Chathurangi

####REG.NO : IT12081530

####SUBJECT : ENTERPRISE STANDARDS AND BEST PRACTICES FOR IT INFRASTRUCTURE

####LAB : 01

#CREATING AN AMAZON EBS-BACKED WINDOWS AMI

###Launching an Instance

1.Open the Amazon EC2 console

![1](https://cloud.githubusercontent.com/assets/13193749/8743177/61638b62-2c8a-11e5-8e17-a0e7ef9a67ac.png)

2.In the navigation bar at the top of the screen, the current region is displayed. Select the region for the instance. 

![2](https://cloud.githubusercontent.com/assets/13193749/8743754/4190c5ca-2c8f-11e5-8d06-a05a640b2d28.png)

3.From the Amazon EC2 console dashboard, click Launch Instance.
![3](https://cloud.githubusercontent.com/assets/13193749/8743178/61887f12-2c8a-11e5-863e-f5f304745632.png)

4.On the Choose an Amazon Machine Image (AMI) page, choose an AMI(Microsoft Windows Server 2012 Base).
![4](https://cloud.githubusercontent.com/assets/13193749/8743180/61c9c0a8-2c8a-11e5-84d7-da48afbc6ea2.png)

5.On the Choose an Instance Type page, select the hardware configuration and size of the instance to launch. Eligible for the free tier, select the t2.micro instance type. Note --> Set up an instance quickly for testing purposes, you can click Review and Launch at this point to accept default configuration settings, and launch your instance.

To configure your instance further, click Next: Configure Instance Details.
![5](https://cloud.githubusercontent.com/assets/13193749/8743181/61e16d3e-2c8a-11e5-9486-380054e3251f.png)

6.On the Configure Instance Details page, change the settings as necessary and then click Next. ( Here I have selected the default configuration settings )
![6](https://cloud.githubusercontent.com/assets/13193749/8743182/6221b060-2c8a-11e5-9bcd-1ca76cb5de89.png)

7.On the Add Storage page, you can specify volumes to attach to the instance besides the volumes specified by the AMI (such as the root device volume) then click Next: Tag Instance when you have finished.
![7](https://cloud.githubusercontent.com/assets/13193749/8743183/622d4d9e-2c8a-11e5-918a-f2459e60c03f.png)

8.On the Configure Security Group page, use a security group to define firewall rules for your instance. These rules specify which incoming network traffic is delivered to your instance. All other traffic is ignored. Select or create a security group and then click Review and Launch.

Here I have selected create a new security group.

In Create a new security group the wizard automatically defines the launch-wizard-x security group.You can edit the name and description of the security group.
Here I have edited the name and the description as shown in the prints screen.

The wizard automatically defines an inbound rule to allow to you connect to your instance over SSH (port 22) for Linux or RDP (port 3389) for Windows.

![8](https://cloud.githubusercontent.com/assets/13193749/8743189/64619c14-2c8a-11e5-813d-498c1d4d17dc.png)

9.On the Review Instance Launch page, check the details of your instance, and make any necessary changes by clicking the appropriate Edit link.When you are ready, click Launch.

10.In the Select an existing key pair or create a new key pair dialog box, you can choose an existing key pair, or create a new one. Here I have created a new key pair.

To launch your instance, select the acknowledgment check box, then click Launch Instances.

Note --> If you select the Proceed without key pair option, you won't be able to connect to the instance unless you choose an AMI that is configured to allow users another way to log in.

11.Launch Instance



### Connect Using Remote Desktop

1. Connect Using Remote Desktop
![9](https://cloud.githubusercontent.com/assets/13193749/8743196/66fa1fe6-2c8a-11e5-8a9c-1aa8fec63182.png)

2. Logging to the remote desktop
![10](https://cloud.githubusercontent.com/assets/13193749/8743184/62fb807e-2c8a-11e5-9b1f-6adefbd7ec8c.png)

![11](https://cloud.githubusercontent.com/assets/13193749/8743193/65f2736e-2c8a-11e5-8293-3569ecfe2ab3.png)

3.Connecting to the virtual machine in cloud
![12](https://cloud.githubusercontent.com/assets/13193749/8743146/3f0c37e4-2c8a-11e5-9a72-9e6f13512555.png)
 
4.Can change the server password
![13](https://cloud.githubusercontent.com/assets/13193749/8743148/3f479564-2c8a-11e5-829d-e7d233b55394.png)



### Connect Using SSH

![14](https://cloud.githubusercontent.com/assets/13193749/8743151/3ff1868c-2c8a-11e5-887b-e64fb4328c34.png)

![15](https://cloud.githubusercontent.com/assets/13193749/8743152/403e7050-2c8a-11e5-9691-3ed940d0f130.png)

![16](https://cloud.githubusercontent.com/assets/13193749/8743153/408f48fe-2c8a-11e5-9add-661a5e56370a.png)

* In command prompt type nslookup and check resolutions
![17](https://cloud.githubusercontent.com/assets/13193749/8743154/40ee8bfc-2c8a-11e5-9aae-5dc6beb3352a.png)


