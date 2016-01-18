## Installing Tricky Python 2.7 Dependencies on Your AWS EC2 Instance
### For Amazon Linux AMI (CentOS, not Ubuntu)
*Updated January 14, 2016* <br><br>
**1. Install the following, in this order:**<br>
`sudo yum install gcc` <br>
`sudo yum install mysql mysql-devel mysql-libs` <br>
`sudo yum install python-devel` <br>
`sudo yum install MySQL-python` <br>
`sudo pip install mysql-python` <br><br>

**2. Upgrade pip and set the correct path** <br>
`sudo pip install --upgrade` <br><br>
When you upgrade pip on an EC2 instance, your `sudo pip` will be broken. To set the correct path, look at my answer on StackOverflow: http://stackoverflow.com/questions/34103119/upgrade-pip-in-amazon-linux/34584537#34584537 <br><br>

**3. Install numpy** <br>
`sudo yum install python27-numpy`<br><br>

**4. Install scipy** <br>
`sudo yum install python27-scipy` <br><br>

**5. Install matplotlib** <br>
`sudo yum install python27-matplotlib` <br><br>
