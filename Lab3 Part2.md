####NAME : K.D.D. Chathurangi

####REG.NO : IT12081530

####SUBJECT : ENTERPRISE STANDARDS AND BEST PRACTICES FOR IT INFRASTRUCTURE

####LAB : 03 Part2

#Creating a DB Instance Running the MySQL Database Engine
##AWS Management Console
###To launch a MySQL DB instance

1. Sign in to the AWS Management Console and open the Amazon RDS console at https://console.aws.amazon.com/rds/.
2. In the top right corner of the AWS Management Console, select the region in which you want to create the DB instance. 

![1](https://cloud.githubusercontent.com/assets/13193749/8902266/2c0fdb10-346d-11e5-87f0-7e5338281ad9.png)

3.In the navigation pane, click DB Instances.

![2](https://cloud.githubusercontent.com/assets/13193749/8902259/2be732dc-346d-11e5-88e0-dc40f0e74bfc.png)

4.Click Launch DB Instance to start the Launch DB Instance Wizard.

![3](https://cloud.githubusercontent.com/assets/13193749/8902268/2c111520-346d-11e5-9e0f-34fbe8c28190.png)

The wizard opens on the Select Engine page. 

![4](https://cloud.githubusercontent.com/assets/13193749/8902267/2c103178-346d-11e5-9740-a890d05bcd01.png)

5.In the Launch DB Instance Wizard window, click the Select button for the MySQL DB engine.

6.The next step asks if you are planning to use the DB instance you are creating for production. If you are, select Yes. By selecting Yes, the failover option Multi-AZ and the Provisioned IOPS storage option will be preselected in the following step. Click Next when you are finished.

![5](https://cloud.githubusercontent.com/assets/13193749/8902269/2c166b42-346d-11e5-9b7b-b8d85ed19bcf.png)

7.On the Specify DB Details page, specify your DB instance information. 

![6](https://cloud.githubusercontent.com/assets/13193749/8902270/2c17d2e8-346d-11e5-9a2d-5b516b463183.png)
![7](https://cloud.githubusercontent.com/assets/13193749/8902271/2c250314-346d-11e5-828c-e487614d01bd.png)

8.On the Configure Advanced Settings page, provide additional information that RDS needs to launch the MySQL DB instance.Specify your DB instance information, then click Next Step

![8](https://cloud.githubusercontent.com/assets/13193749/8902273/2c3140b6-346d-11e5-92c2-35767f3eb2b1.png)

![9](https://cloud.githubusercontent.com/assets/13193749/8902274/2c356fce-346d-11e5-9ea8-ef55115c9603.png)

![10](https://cloud.githubusercontent.com/assets/13193749/8902275/2c3724ea-346d-11e5-80f2-1635dd57bbd7.png)

9.Click Launch DB Instance to create your MySQL DB instance.

![11](https://cloud.githubusercontent.com/assets/13193749/8902277/2c3c5ac8-346d-11e5-9e35-c139d331fb5b.png)

10.On the final page of the wizard, click Close. 

11.On the Amazon RDS console, the new DB instance appears in the list of DB instances. The DB instance will have a status of creating until the DB instance is created and ready for use. When the state changes to available, you can connect to the DB instance. Depending on the DB instance class and store allocated, it could take several minutes for the new instance to be available.

![12](https://cloud.githubusercontent.com/assets/13193749/8902279/2c413afc-346d-11e5-923d-1bebd67a17d7.png)

![13](https://cloud.githubusercontent.com/assets/13193749/8902278/2c40d79c-346d-11e5-97f5-2c563aa5f7b4.png)

![14](https://cloud.githubusercontent.com/assets/13193749/8902280/2c41ac76-346d-11e5-82fc-a84a965185bf.png)

![15](https://cloud.githubusercontent.com/assets/13193749/8902281/2c44b916-346d-11e5-8614-823ab0d2251c.png)

12.Deleting a DB Instance

![16](https://cloud.githubusercontent.com/assets/13193749/8902282/2c4a76e4-346d-11e5-860b-0cb5d806e3a7.png)

#Microsoft SQL Server on Amazon RDS

![17](https://cloud.githubusercontent.com/assets/13193749/8902254/2bd95c02-346d-11e5-9f60-887b8322d09a.png)

##Connecting to a DB Instance Running the SQL Server Database Engine

####Connecting with SQL Server Management Studio

To connect to a DB instance using Microsoft SQL Server Management Studio

1. On the Instances page of the AWS Management Console, select the arrow next to the DB instance
to show the instance details. Note the server name and port of the DB instance, which are displayed
in the Endpoint field at the top of the panel, and the master user name, which is displayed in the
Username field in the Configuration Details section. An example is shown following:

![](https://cloud.githubusercontent.com/assets/13193749/8902252/2b858eba-346d-11e5-8f32-40462bc44cd3.png)

2 . Open Microsoft SQL Server Management Studio. The Connect to Server dialog box appears, as shown following:

![](https://cloud.githubusercontent.com/assets/13193749/8902260/2bfa3198-346d-11e5-8fd0-f47197e46f5d.png)

3 . In the Server type: box, select Database Engine.

4 . In the Server name box, type or paste the server name of the DB instance, type a comma ",", and
then type the port number used by the DB instance. For example, the Server name value could be:
sqlsvr-pdz.abcd12340.us-west-2.rds.amazonaws.com,1433.

![](https://cloud.githubusercontent.com/assets/13193749/8902261/2bfd0a62-346d-11e5-9114-d4d14ff8be4a.png)

5 . In the Authentication box, select SQL Server Authentication.

6 . In the Login box, type or paste the master user name for the DB instance.

7 . In the Password box, type the password for the master user.

8 . Click Connect. After a few moments, Microsoft SQL Server Management Studio should be connected
to your DB instance.
9. Click New Query in the SQL Server Management Studio toolbar, as shown following:

![](https://cloud.githubusercontent.com/assets/13193749/8902262/2c026eee-346d-11e5-9a50-5a1586dc09e4.png)
A new SQL query window will open.

10. Type the following SQL query:

#####select @@VERSION

![](https://cloud.githubusercontent.com/assets/13193749/8902263/2c03247e-346d-11e5-944f-abcb1800a299.png)

11 . Click ! Execute on the SQL Enterprise Manager toolbar to run the query, as shown following:

![](https://cloud.githubusercontent.com/assets/13193749/8902264/2c04bef6-346d-11e5-9b15-655117cc330d.png)

The query should return the version information for your DB instance
