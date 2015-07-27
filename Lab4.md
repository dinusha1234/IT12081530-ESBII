####NAME : K.D.D. Chathurangi

####REG.NO : IT12081530

####SUBJECT : ENTERPRISE STANDARDS AND BEST PRACTICES FOR IT INFRASTRUCTURE

####LAB : 04


Get accounts and install software

    Install Git
    Get a GitHub account
    Install the Sublime Text 2 text editor
    Install VirtualBox
    Install Vagrant

###Download IntroHCI configuration files
* Download setup files at http://d.ucsd.edu/class/intro-hci/2015/vagrant.zip

* Unzip that folder 

![1](https://cloud.githubusercontent.com/assets/13193749/8899223/20a25a46-344f-11e5-8085-83d48cb35d58.png)

* Fork your first repository
Find Lab 1 at https://github.com/IntroHCI/lab1.
Forking will clone the repository in your Github account

![2](https://cloud.githubusercontent.com/assets/13193749/8899473/859cead0-3452-11e5-81ca-137c8b033921.png)

![3](https://cloud.githubusercontent.com/assets/13193749/8899470/83b72dca-3452-11e5-8e15-65920d4cdaf8.png)

*  Copy the git clone URL
     Make sure you copy the git clone url of the repository that you just forked. The url should be something like this: https://github.com/your_user_name_/lab1.git instead of https://github.com/IntroHCL/lab1.git


In my case the URL is 
https://github.com/dinusha1234/lab1.git

![4](https://cloud.githubusercontent.com/assets/13193749/8899471/845c4c24-3452-11e5-91ce-d40aa202ce4a.png)

Later on push the change to Github, but you won't be able to do that if you cloned the orginal repo down, since you are not the owner of the orginal repo.

### Open your terminal
* go to introHCI in the Documents and view the contents

![5](https://cloud.githubusercontent.com/assets/13193749/8899226/20a6db8e-344f-11e5-8724-44e9deced2bc.png)

### git clone the repo inside of introHCI
* Make sure the clone URL has your forked GitHub username in it, not IntroHCI

![6](https://cloud.githubusercontent.com/assets/13193749/8899227/20ac0532-344f-11e5-87b9-600fe2c66c62.png)

### Open your text editor
My one is linux so first go to Start Menu-> Sublime Text 2

### Add your info into lab1/static/index.html
* This HTML will be redered by the server

![7](https://cloud.githubusercontent.com/assets/13193749/8899228/20b8611a-344f-11e5-93b2-f5537a1ef217.png)

### Browse to index.html using the file on your hard drive

![8](https://cloud.githubusercontent.com/assets/13193749/8899202/20338102-344f-11e5-8dfd-cf09ee154dd8.png)

### Set up Git so can commit

![9](https://cloud.githubusercontent.com/assets/13193749/8899203/2038385a-344f-11e5-894a-7a2dd7ff75b6.png)

![10](https://cloud.githubusercontent.com/assets/13193749/8899206/20423530-344f-11e5-9615-adf78955c974.png)

### GitHub reflects your commit

![11](https://cloud.githubusercontent.com/assets/13193749/8899819/dbc0e962-3456-11e5-9a2a-ecd0b4aff46e.png)

#####Preparing Server
###Why are we using a virtual machine?
#######1.Multiple choice:
* Because we want to prove how little RAM you actually have.
* Because we enjoy creating little universes inside your computer
* Because Linux is t3h I337 h4XX0r software
* Because we can prepackage everything you will need for the class and support one version of all the software

#######2. Vagrant hosts an Ubuntu Linux machine for us and provides nice interfaces for shared folders and administrator.

###Autoupgrade the VirtualBox guest tools
* Install the vbguest plugin for VirtualBox guest tools.

![12](https://cloud.githubusercontent.com/assets/13193749/8899214/20736c9a-344f-11e5-9b14-8861838732cc.png)

###Run vagrant up in the introHCL directory

![13](https://cloud.githubusercontent.com/assets/13193749/8899214/20736c9a-344f-11e5-9b14-8861838732cc.png)

![14](https://cloud.githubusercontent.com/assets/13193749/8899215/20756ab8-344f-11e5-8597-4050c50552a0.png)

![15](https://cloud.githubusercontent.com/assets/13193749/8899218/208d3cc4-344f-11e5-8e3d-5074c5ff8583.png)

