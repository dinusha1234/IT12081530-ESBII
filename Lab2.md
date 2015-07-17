####NAME : K.D.D. Chathurangi

####REG.NO : IT12081530

####SUBJECT : ENTERPRISE STANDARDS AND BEST PRACTICES FOR IT INFRASTRUCTURE

####LAB : 02

#CREATING AN AMAZON EBS-BACKED LINUX AMI

###Launching an Instance

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
2. Find and load your ‘.pem’ file; it’s probably in your Downloads folder. Note, you have to select ‘All files’ on the bottom.
3. Load it.

4. Now, “save private key”. Put it somewhere easy to find.

###Logging into your EC2 instance with Putty

1.Open up putty, and enter your hostname into the Host Name box.

2.Now, go find the ‘SSH’ section and enter your ppk file (generated above by puttygen). Then select ‘Open’.




###Creating the AMI from an Instance


* In the navigation pane, click Instances and select your instance. Click Actions, select Image, and then click Create Image.


* In the Create Image dialog box, specify the following, and then click Create Image.

    1.  A unique name for the image.

    2.  A description of the image, up to 255 characters.

    3. By default, Amazon EC2 shuts down the instance, takes snapshots of any attached volumes, creates and registers the AMI, and then reboots the instance. Select No reboot if you don't want your instance to be shut down.

    4. Click AMIs in the navigation pane to view the status of your AMI. While the new AMI is being created, its status is pending. This process typically takes a few minutes to finish, and then the status of your AMI is available.

    5. Click Snapshots in the navigation pane to view the snapshot that was created for the new AMI. When you launch an instance from this AMI, we use this snapshot to create its root device volume.

###Creating an AMI from a Snapshot
1. Open the Amazon EC2 console at https://console.aws.amazon.com/ec2/.

2. In the navigation pane, under Elastic Block Store, choose Snapshots.

3. Choose the snapshot, and then choose Create Image from the Actions list.

4. In the Create Image from EBS Snapshot dialog box, complete the fields to create your AMI, then choose Create. If you're re-creating a parent instance, then choose the same options as the parent instance.

    * Architecture: Choose i386 for 32-bit or x86_64 for 64-bit.

    * Root device name: Enter the appropriate name for the root volume. For more information, see Device Naming on Linux Instances.

    * Virtualization type: Choose whether instances launched from this AMI use paravirtual (PV) or hardware virtual machine (HVM) virtualization. For more information, see Linux AMI Virtualization Types.

    * (PV virtualization type only) Kernel ID and RAM disk ID: Choose the AKI and ARI from the lists. If you choose the default AKI or don't choose an AKI, you'll be required to specify an AKI every time you launch an instance using this AMI. In addition, your instance may fail the health checks if the default AKI is incompatible with the instance.

    * Block Device Mappings: Add volumes or expand the default size of the root volume for the AMI. For more information about resizing the file system on your instance for a larger volume, see Extending a Linux File System



