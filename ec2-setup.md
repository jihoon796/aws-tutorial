# EC2 Instance Setup

Before we can setup an EC2 instance, you will need to create an AWS account at https://aws.amazon.com/

Once you've signed up for an AWS account, go to *My Account* on the top right corner, and click on *AWS Management Console*. It's a good idea to bookmark the management console, because it'll be useful in the future. While you're in the management console, be sure to edit your location settings (if applicable) - your location is set to Oregon by default, so make sure to bookmark to correct page!

To begin setting up your EC2 instance, click on *EC2* on the left side of the page. You'll be taken to the EC2 management console, where you can start your instance by clicking *Launch Instance*. 


**Step 1: Choose an Amazon Machine Image (AMI)**

Choosing an AMI basically means choosing the type of computer and operating system you will work with. There are pros and cons to each of the choices listed, but you can't really go wrong with any of the Linux distributions like Red Hat Enterprise, SUSE, and Ubuntu. "Amazon Linux" itself similar to CentOS (another Linux distro) and is essentially a minimalistic install of Red Hat Enterprise Linux (RHEL).

Personally speaking, I chose the **Amazon Linux AMI** because it seems well-suited and optimized for working with AWS.


**Step 2: Choose an Instance Type**

This really depends on what you want to do. For the most part, **t2.micro**, **t2.small**, or **t2.medium** should be enough to do anything you need. You can always upgrade/downgrade the instances as needed in the future!




