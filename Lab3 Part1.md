####NAME : K.D.D. Chathurangi

####REG.NO : IT12081530

####SUBJECT : ENTERPRISE STANDARDS AND BEST PRACTICES FOR IT INFRASTRUCTURE

####LAB : 03 Part1

#Create a Bucket

###To create a bucket

1. Sign into the AWS Management Console and open the Amazon S3 console at https://console.aws.amazon.com/s3.

2.  In the Create a Bucket dialog box, in the Bucket Name box, enter a bucket name.The bucket name you choose must be unique across all existing bucket names in Amazon S3

Note

After you create a bucket, you cannot change its name. In addition, the bucket name is visible in the URL that points to the objects stored in the bucket. Ensure that the bucket name you choose is appropriate. 

3 . In the Region box, select a region. For this exercise, select Oregon from the drop-down list.

![1](https://cloud.githubusercontent.com/assets/13193749/8900337/975c054e-345c-11e5-80e5-fda2bde99bf2.png)

4.Click Create.

When Amazon S3 successfully creates your bucket, the console displays your empty bucket in the Buckets panel.

###Add an Object to a Bucket

Now that you've created a bucket, you're ready to add an object to it. An object can be any kind of file: a text file, a photo, a video and so forth. When you add a file to Amazon S3, you have the option of including metadata with the file and setting permissions to control access to the file.

#####To upload an object

1. In the Amazon S3 console, click the name of bucket that you want to upload an object to and then click Upload.

![2](https://cloud.githubusercontent.com/assets/13193749/8900332/974e6182-345c-11e5-9011-b8ef2fdcdd09.png)

2.In the Upload - Select Files wizard, if you want to upload an entire folder, you must click Enable Enhanced Uploader to install the necessary Java applet. You only need to do this once per console session

![3](https://cloud.githubusercontent.com/assets/13193749/8900334/9754b442-345c-11e5-815d-2c2252687aff.png)

3.Click Add Files.

4.Select the file that you want to upload and then click Open.

5.Click Start Upload.

You can watch the progress of the upload from within the Transfer panel.

![4](https://cloud.githubusercontent.com/assets/13193749/8900336/9757f5ee-345c-11e5-81c4-8fd9c3efa944.png)

![5](https://cloud.githubusercontent.com/assets/13193749/8900338/976187a8-345c-11e5-99ba-31c4db1a1013.png)

###View an Object

Now that you've added an object to a bucket, you can open and view it in a browser. You can also download the object to your local computer.

#####To open or download an object

1. In the Amazon S3 console, in the Objects and Folders list, right-click the object or objects that you want to open or download, then click Open or Download as appropriate.

![6](https://cloud.githubusercontent.com/assets/13193749/8900343/977d3822-345c-11e5-8153-259ba45d7c9d.png)

![7](https://cloud.githubusercontent.com/assets/13193749/8900344/978008c2-345c-11e5-9c48-1bd991083400.png)

2.If you are downloading the object, specify where you want to save it. The procedure for saving the object depends on the browser and operating system that you are using.

![8](https://cloud.githubusercontent.com/assets/13193749/8900345/9781ef70-345c-11e5-8493-ef9b91eee9df.png)

Note

By default, your Amazon S3 buckets and objects are private. To make an object viewable by using a URL, for example, https://s3.amazonaws.com/Bucket/Object, you must make the object publicly readable.

![9](https://cloud.githubusercontent.com/assets/13193749/8900346/9787307a-345c-11e5-97ee-24464ed188a7.png)

#####To make an object accessible by everyone

![10](https://cloud.githubusercontent.com/assets/13193749/8900341/976a7c6e-345c-11e5-9a18-b88254aac2d4.png)


The console provides a shortcut for making objects accessible to everyone, meaning that everyone can both view and download the object.

1.Right-click the object that you want to make accessible, and then click Make Public.

![11](https://cloud.githubusercontent.com/assets/13193749/8900342/9776771c-345c-11e5-9189-bd6c219d436f.png)

###Move an Object

Now that you've added an object to a bucket and viewed it, you can move the object to a different bucket or folder.

Note

In this exercise, you work with one object; however, you can also follow these steps for moving a folder.

#####To move an object

1.In the Amazon S3 console, right-click the object that you want to move, and then click Cut.

Tip

You can use the SHIFT and CTRL keys to select multiple objects and perform the same action on them simultaneously.

![12](https://cloud.githubusercontent.com/assets/13193749/8900326/97223468-345c-11e5-8237-a7b4f15b41aa.png)

![13](https://cloud.githubusercontent.com/assets/13193749/8900325/971e8624-345c-11e5-8878-f486ac5a3765.png)

![14](https://cloud.githubusercontent.com/assets/13193749/8900328/972c3ad0-345c-11e5-9152-3238a8feaad8.png)

###Delete an Object and Bucket

If you no longer need to store the objects that you uploaded and moved while going through this guide, you should delete them to prevent further charges.

#####To delete an object

1. Sign in to the AWS Management Console and open the Amazon S3 console at https://console.aws.amazon.com/s3/.

2. In the Objects and Folders panel, right-click the object that you want to delete, and then click Delete.

![15](https://cloud.githubusercontent.com/assets/13193749/8900330/972e0ef0-345c-11e5-8625-f43c7273e1b8.png)

![16](https://cloud.githubusercontent.com/assets/13193749/8900329/972d0514-345c-11e5-86cb-44800dafd8e4.png)
#####To empty a bucket

1.Sign in to the AWS Management Console and open the Amazon S3 console at https://console.aws.amazon.com/s3/.

2.Right-click the bucket that you want to empty, and then click Empty Bucket.

3.When a confirmation message appears, enter the bucket name and then click Empty bucket.

![17](https://cloud.githubusercontent.com/assets/13193749/8900335/9755e07e-345c-11e5-87ec-72e9c23c128a.png) 

###To delete a bucket

1.Sign in to the AWS Management Console and open the Amazon S3 console at https://console.aws.amazon.com/s3/.

2.Right-click the bucket that you want to delete, and then click Delete Bucket.

![18](https://cloud.githubusercontent.com/assets/13193749/8900333/974eb420-345c-11e5-8ee6-25646f737497.png) 

3.When a confirmation message appears, enter the bucket name and then click Empty bucket.

![19](https://cloud.githubusercontent.com/assets/13193749/8900339/976269d4-345c-11e5-854b-9baecb1d2382.png)

![20](https://cloud.githubusercontent.com/assets/13193749/8900331/97481d0e-345c-11e5-9a4f-4670c8305ac7.png)