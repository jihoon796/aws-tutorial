## Installing Tricky Python Dependencies for Your AWS EC2 Instance

**1. Install the following, in this order:**

`sudo yum install gcc` <br>
`sudo yum install mysql mysql-devel mysql-libs` <br>
`sudo yum install python-devel` <br>
`sudo yum install MySQL-python` <br>
`sudo pip install mysql-python` <br>

**2. Upgrade pip and set the correct path** <br>
To upgrade: `sudo pip install --upgrade` <br><br>
When you upgrade pip on an EC2 instance, your `sudo pip` will be broken. To set the correct path, look at my answer on StackOverflow: http://stackoverflow.com/questions/34103119/upgrade-pip-in-amazon-linux/34584537#34584537


**3. Install numpy** <br>
`sudo yum install python27-numpy`

**4. Install scipy** <br>
`sudo yum install python27-scipy`
