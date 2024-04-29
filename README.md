# Deploying-Web-App-on-Azure
Creation of a Linux virtual machine on your free Azure account, install a web server on the virtual machine, and deploy a web application

## Steps 
1. Get an Azure account, free accounts available in 2 ways: (1) A general account with a credit card required, which provides some free services for 12 month and $200 Azure credit for 30 days.(2) A student account associated with your university email with no credit card required, which starts with $100 Azure credit.
2. Create a virtual machine with the cloud platform provided by Azure. During creation ensure that the ports 80 is accessible. Also ensure that a key.pem file is created.
3. Download the Files from my GITHUB Repo into your local machine.
4. Login into the Azure VM using the command prompt:   ssh -i .\myKey.pem azureuser@52.173.20.0 (Replace .\myKey.pem with the correct path to your key.pem file, and the IP address after the '@' replace it with the IP generated for your VM.)
5. Transfer the files from the local machine into the Azure VM via command prompt. scp -i myKey.pem index.html azureuser@52.173.20.0: scp -i myKey.pem routes.js azureuser@52.173.20.0:(again replace the myKey.pem and the @52.173.20.0 with the correct info for your account.)
6. Move a file from your account root folder to the default root folder of the web server:sudo cp index.html /var/www/html
