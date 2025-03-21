# Senthilkumar AWS CICD Pipeline Code Deployment to AWS EC2 Instance
# Ensures that the EC2 instance is ready to be used with AWS CodeDeploy for automating deployments.
# Installs AWS CLI to interact with AWS services programmatically.
# Automatically executes at the first boot of the EC2 instance.


<b>User Data for Dependencies installations for AMAZON Linux 2:-</b>

#!/bin/bash<br />
sudo yum -y update<br />
sudo yum -y install ruby<br />
sudo yum -y install wget<br />
cd /home/ec2-user<br />
wget https://aws-codedeploy-ap-south-1.s3.ap-south-1.amazonaws.com/latest/install<br />
sudo chmod +x ./install<br />
sudo ./install auto<br />
sudo yum install -y python-pip<br />
sudo pip install awscli<br />
