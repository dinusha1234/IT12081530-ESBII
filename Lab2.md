####NAME : K.D.D. Chathurangi

####REG.NO : IT12081530

####SUBJECT : ENTERPRISE STANDARDS AND BEST PRACTICES FOR IT INFRASTRUCTURE

####LAB : 02

#CREATING AN AMAZON EBS-BACKED LINUX AMI

###Launching an Instance

* select Amazon Linux AMI 2015.03(GVM)
![](https://cloud.githubusercontent.com/assets/13193749/8743156/4190e9b0-2c8a-11e5-81db-a1a1365017d3.png)

![](https://cloud.githubusercontent.com/assets/13193749/8743187/63794428-2c8a-11e5-999a-1fbc0fd956db.png)

![](https://cloud.githubusercontent.com/assets/13193749/8743188/63d9c7d0-2c8a-11e5-8b9d-ed424544edfc.png)
 
![](https://cloud.githubusercontent.com/assets/13193749/8743197/6763f3d0-2c8a-11e5-85fb-53e96dfd2240.png)

####CONNECT TO THE INSTANCE AND CUSTOMIZE IT

**PREREQUISITES

Before you connect to your Linux instance using PuTTY, complete the following prerequisites:**

1.Install PuTTY Download and install PuTTY

2.Get the ID of the instance u can get the ID of your instance using the Amazon EC2 console

3.Get the public DNS name of the instance You can get the public DNS for your instance using the Amazon EC2 console (check the Public DNS column; if this column is hidden, click the Show/Hide icon and select Public DNS)

4.Locate the private key your IP address to your instance You'll need the fully-qualified path of the .pem file for the key pair that you specified when you launched the instance.

5.Enable inbound SSH traffic from 

####Logging into your new instance “in the cloud” (Windows version)

 Generate a ppk file from your pem file

1. Open puttygen; select “Load”.
![](https://cloud.githubusercontent.com/assets/13193749/8743173/60a14cfa-2c8a-11e5-966b-91b0b2bcaa0e.png)

2. Find and load your ‘.pem’ file; it’s probably in your Downloads folder. Note, you have to select ‘All files’ on the bottom.
![](https://cloud.githubusercontent.com/assets/13193749/8743176/61545d72-2c8a-11e5-8095-b70d219105b0.png)

3. Load it.
![](https://cloud.githubusercontent.com/assets/13193749/8743175/6123aefc-2c8a-11e5-846c-373a7943c6bd.png)

4. Now, “save private key”. Put it somewhere easy to find.
![](https://cloud.githubusercontent.com/assets/13193749/8743174/60cb0bd0-2c8a-11e5-9362-ea3b8366e67b.png)

###Logging into your EC2 instance with Putty

1.Open up putty, and enter your hostname into the Host Name box.
![](https://cloud.githubusercontent.com/assets/13193749/8743190/64be1976-2c8a-11e5-8476-4124df0888d3.png)

2.Now, go find the ‘SSH’ section and enter your ppk file (generated above by puttygen). Then select ‘Open’.

![](https://cloud.githubusercontent.com/assets/13193749/8743195/668b0458-2c8a-11e5-9947-18ea42379be5.png)

3.Finally, can connecting to Linux instance

![](https://cloud.githubusercontent.com/assets/13193749/8744168/b20c4af6-2c92-11e5-8708-bc720f87319a.png)


###Creating the AMI from an Instance


* In the navigation pane, click Instances and select your instance. Click Actions, select Image, and then click Create Image.


* In the Create Image dialog box, specify the following, and then click Create Image.

    1.  A unique name for the image.
![](https://cloud.githubusercontent.com/assets/13193749/8743192/6576066c-2c8a-11e5-83f9-1e49eee65272.png)

    2.  A description of the image, up to 255 characters.Then Click Create

![](https://cloud.githubusercontent.com/assets/13193749/8743191/650c7788-2c8a-11e5-9287-82988c64c996.png)

    3. By default, Amazon EC2 shuts down the instance, takes snapshots of any attached volumes, creates and registers the AMI, and then reboots the instance. Select No reboot if you don't want your instance to be shut down.

    4. Click AMIs in the navigation pane to view the status of your AMI. While the new AMI is being created, its status is pending. This process typically takes a few minutes to finish, and then the status of your AMI is available.

![](https://cloud.githubusercontent.com/assets/13193749/8745279/d8cd7170-2c9b-11e5-9a36-f542c6644c98.png)

    5. Click Snapshots in the navigation pane to view the snapshot that was created for the new AMI. When you launch an instance from this AMI, we use this snapshot to create its root device volume.

![](https://cloud.githubusercontent.com/assets/13193749/8745359/d2875ae6-2c9c-11e5-8ecd-efc8d795e592.png)

###Creating an AMI from a Snapshot
1. Open the Amazon EC2 console at https://console.aws.amazon.com/ec2/.

2. In the navigation pane, under Elastic Block Store, choose Snapshots.

3. Choose the snapshot, and then choose Create Image from the Actions list.
![](https://cloud.githubusercontent.com/assets/13193749/8744968/eeb0215c-2c98-11e5-948e-00788dec7025.png)

4. In the Create Image from EBS Snapshot dialog box, complete the fields to create your AMI, then choose Create. If you're re-creating a parent instance, then choose the same options as the parent instance.

    * Architecture: Choose i386 for 32-bit or x86_64 for 64-bit.

    * Root device name: Enter the appropriate name for the root volume. For more information, see Device Naming on Linux Instances.

    * Virtualization type: Choose whether instances launched from this AMI use paravirtual (PV) or hardware virtual machine (HVM) virtualization. For more information, see Linux AMI Virtualization Types.

    * (PV virtualization type only) Kernel ID and RAM disk ID: Choose the AKI and ARI from the lists. If you choose the default AKI or don't choose an AKI, you'll be required to specify an AKI every time you launch an instance using this AMI. In addition, your instance may fail the health checks if the default AKI is incompatible with the instance.

    * Block Device Mappings: Add volumes or expand the default size of the root volume for the AMI. For more information about resizing the file system on your instance for a larger volume, see Extending a Linux File System
    
![](https://cloud.githubusercontent.com/assets/13193749/8744969/ef0accba-2c98-11e5-8f2f-942c80e92797.png)

![](https://cloud.githubusercontent.com/assets/13193749/8744970/ef457e82-2c98-11e5-99ae-6ed94279f57e.png)

![](https://cloud.githubusercontent.com/assets/13193749/8744971/ef95f0e2-2c98-11e5-8aa1-d02aee7ff3fb.png)

