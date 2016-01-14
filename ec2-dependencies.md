## Installing Tricky Python Dependencies for Your AWS EC2 Instance

**1. Install the following, in this order:**

`sudo yum install gcc` <br>
`sudo yum install mysql mysql-devel mysql-libs` <br>
`sudo yum install python-devel` <br>
`sudo yum install MySQL-python` <br>
`sudo pip install mysql-python` <br>

**2. Upgrade pip - set the correct path for** `sudo pip`

**3. Install numpy** <br>
`sudo yum install python27-numpy`

**4. Install scipy** <br>
`sudo yum install python27-scipy`
