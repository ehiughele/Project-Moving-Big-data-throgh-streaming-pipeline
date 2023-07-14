ssh -i ec2-de-mbd-predict-key.pem ec2-user@ec2-34-248-145-7.eu-west-1.compute.amazonaws.com

chmod 400 ec2-de-mbd-predict-key.pem
this first step

_____________________________________________________________
…or create a new repository on the command line

echo "# Moving-Big-Data" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/ehiughele/Moving-Big-Data.git
git push -u origin main


________________________________________________________________
…or push an existing repository from the command line

git remote add origin https://github.com/ehiughele/Moving-Big-Data.git
git branch -M main
git push -u origin main


__________________________________________________________________
HOW TO INSTALL ANACONDA ON EC2 INSTALL
STEP 1 ==> open command prompt... navigate to directory where .pem file is stored

cd C:\Users\HP\Downloads\Moving Big Data

Step 2 ==> Log in to your ec2 instance via ssh

ssh -i ec2-de-mbd-predict-key.pem ec2-user@ec2-34-248-145-7.eu-west-1.compute.amazonaws.com

Step 3 ==> follow the steps for the link https://medium.com/@GalarnykMichael/aws-ec2-part-3-installing-anaconda-on-ec2-linux-ubuntu-dbef0835818a

https://repo.anaconda.com/archive/

wget https://repo.anaconda.com/archive/Anaconda2-4.1.1-Linux-x86_64.sh

then type
bash Anaconda2-4.1.1-Linux-x86_64.sh

______________________________________________________________________
HOW TO INSTALL PANDAS ON EC2 INSTALL

Step 1 & 2 ==> as above to login to your ec2 instance

step 3 ==> 

#!/bin/bash
sudo yum install update
sudo yum groupinstall "Development Tools"
sudo yum install python-devel libpng-devel freetype-devel 
	#the last two are necessary for pip to run without failing with 
	#error 'Command "python setup.py egg_info" failed with error code 1'
sudo pip install pandas 	#Finally it works!


Just a quick note, if somebody wants to install it on Python 3, change python-devel to python3-devel and pip to pip3

_____________________________________________________________________
HOW TO INSTALL AWS CLI ON EC2 INSTANCE

https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install

__________________________________________