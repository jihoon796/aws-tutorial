# EC2 Instance Setup
*Updated January 5, 2016*
<br><br>
Before we can setup an EC2 instance, you will need to create an AWS account at https://aws.amazon.com/

Once you've signed up for an AWS account, go to *My Account* on the top right corner, and click on *AWS Management Console*. It's a good idea to bookmark the management console, because it'll be useful in the future. While you're in the management console, be sure to edit your location settings (if applicable) - your location is set to Oregon by default, so make sure to bookmark to correct page!

To begin setting up your EC2 instance, click on *EC2* on the left side of the page. You'll be taken to the EC2 management console, where you can start your instance by clicking *Launch Instance*. 
<br><br>

**Step 1: Choose an Amazon Machine Image (AMI)**

Choosing an AMI basically means choosing the type of computer and operating system you will work with. There are pros and cons to each of the choices listed, but you can't really go wrong with any of the Linux distributions like Red Hat Enterprise, SUSE, and Ubuntu. "Amazon Linux" itself is similar to CentOS (another Linux distro) and is essentially a minimalistic install of Red Hat Enterprise Linux (RHEL).

For this tutorial, please choose the **Amazon Linux AMI** - it seems well-suited and optimized for working with AWS.  
<br>

**Step 2: Choose an Instance Type**

This really depends on what you want to do. For the most part, **t2.micro**, **t2.small**, or **t2.medium** should be enough to do anything you need. You can always upgrade/downgrade the instances as needed in the future!
<br><br>

**Step 3: Review Instance Launch**

If you followed the steps mentioned above, you should've been skipped ahead to step 7 on the AWS console. In this step, we'll configure the **Security Groups** setting. The default security groups setting won't actually allow you to use EC2 through your local machine, so getting this part working is essential.

Click on *Edit security groups* on the bottom right. Once you've done that, click on the *Create a new security group* radio button. Be sure to give your security group a name you won't easily forget, since you may be referring back to this at some point in the future. Go to *Type*, then select the *All traffic* option. Check to see that the *Protocol* is set to *All*, the *Port Range* is set to *0 - 65535*, and the *Source* is *Anywhere*.

Click *Review and Launch* when you are completed. Ignore the next page and click *Launch*.  
<br>

**Step 4: Create a New Key Pair**

Things get a bit tricky here. A key pair is a file that you need to download that is necessary for you to SSH into an EC2 instance. You'll need to create a new key pair and download that key pair into somewhere accessible. I personally recommend downloading that key pair and moving it to your home directory, because that's where it's the most accessible. Again, be sure to name the file something you can remember - the file will have the .pem extension.

Go back to your EC2 management console at https://console.aws.amazon.com/ec2/v2/home and you'll see that you'll have "1 Running Instance" under the Resources section. Click on that, and you'll be taken to a page where you can view your instances. You may have to wait a bit for the instance to actually get set up. Click on the left checkbox on your instance, and details about your instance will pop up in the bottom. Find your *Public DNS* under the *Description* tab. It should be something like **ec2-54-209-134-187.compute-1.amazonaws.com**. Copy the public DNS.


Now locate the directory where the .pem key pair is located (the home directory if you followed my recommendation). Open up your terminal, move to that directory, and type in: ssh -i [your key pair filename] ec2-user@[your public DNS]. 

Your username for the EC2 instance is just ec2-user, so you won't have to change that part. If all goes well, it should look like the below:

```
ssh -i my_key_pair.pem ec2-user@ec2-54-175-186-221.compute-1.amazonaws.com
```

At this point, you should get a welcome message at this point from the Amazon Linux AMI - if you've gotten this far, then congratulations! You have successfully created/started an AWS EC2 instance. You can ```cd``` or ```ls``` and create your own files now. I recommend installing git and using ```git pull``` to pull from a GitHub repository to test things out. The Amazon Linux AMI doesn't come with much, so you'll have to upgrade Python and other such dependencies yourself. 

One gotcha about Amazon Linux is that sudo pip install won't work well - you'll have to follow my directions here: http://stackoverflow.com/questions/34103119/upgrade-pip-in-amazon-linux/34584537#34584537
<br><br>
*The next part of the tutorial will help you set up RDS to work on your computer.*
