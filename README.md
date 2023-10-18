# Cloud Computing Project: Secure File System on Cloud
Cloud Computing and Security (CPSC 454) - Under Professor Yun Tian at California State University - Fullerton


# Steps to run the project:
### Clone the repository:
git clone https://github.com/Debdyuti-01/Secure-File-System-on-Cloud.git

## To run the web application:
### Go to the Web Application directory
cd src/WebApplication
### To run the application
python3 app.py

## To run the StandAlone Application:
### Go to the StandAlone Application directory
cd src/StandAloneApplication
### To run the application
python3 main.py

# Steps to access the application
### Register user on the web application
Click Register-user tab

### Save the private key
After registering, a private key is generated. save that somewhere on your machine

### Download public key
Click Download-public-key tab and check for the user. Download the respective user's public key in your machine.

### To encrypt/decrypt a file
Go to stand-alone application directory in another terminal and run python3 main.py . 
Fill the fields file you want to encrypt/decrypt, public and private key

### Upload to online directory
Click on File-upload tab and upload the encrypted file on the web application

# Debugging Notes
### In case of any error regarding missing installation, perform the following:
pip3 install missingInstallationName
### In case of port error: 
Go to src/WebApplication/app.py
Go to line 168 and change the port number according to your system's availability


