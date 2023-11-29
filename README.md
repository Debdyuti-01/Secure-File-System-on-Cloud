# Cloud Computing Project: Secure File System on Cloud
Cloud Computing and Security (CPSC 454) - Under Professor Yun Tian at California State University - Fullerton


# Steps to run the project:
### Clone the repository:
git clone https://github.com/Debdyuti-01/Secure-File-System-on-Cloud.git

## To run the StandAlone Application:
### Go to the StandAlone Application directory
cd src/StandAloneApplication
### To run the application
python3 main.py

## To run the web application:
### Go to the Web Application directory
cd src/WebApplication
### To run the application
python3 app.py

# Steps to access the application
### Register user on the web application
Click Register-user tab

### Save the private key
After registering, a private key is generated. Save the private key somewhere on your local machine.

### Download public key
Click Download-public-key tab and check for the user. Download the respective user's public key in your machine.

### To encrypt/decrypt a file
Go to stand-alone application directory in another terminal and run python3 main.py . 
Fill the fields file you want to encrypt/decrypt along with public and private key.

### Upload to online directory
Click File-upload tab and upload the encrypted file on the web application

# Steps to host the application on Cloud:
* CReate 
create an amazon EC2 instance.
Select and create Amazon Linux AMI 2018.03.0 (HVM), SSD Volume Type
While creating the machine, toggle to menu Configure Security Group menu.
Here, enable port SSH, HTTP, RDP and in port, change Source to Anywhere
Download and keep the publicKeyPair.pem file
Install putty and puttygen
Open puttygen, select the publicKeyPair.pem and generate a private key. Now, save it as Save private key
Open the AWS machine dashboard ad copy the IPv4 Public IP of the instance created
Open putty
In putty, copy the IP in Host Name(or IP address)
In putty, toggle the SSH>Auth and here, select the private key you generated.
Click open and voila! The terminal of instance opens
Enter "login as:" ec2-user
Enter following command
$sudo bash
$yum install python-pip
$yum install git
$pip install flask
Now, clone the forked repository on local machine
In src/web-application/app.py, comment on line 169 and uncomment line 168
Update the github repository
On the terminal of instance, clone the repository and enter command
$python app.py
