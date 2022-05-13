# Wordpress Installation and Configuration via Ansible 
# on Redhat Linux on AWS

Create the AWS EC2 Instance and connect via SSH

Update and upgrade the linux

`sudo yum update && sudo yum upgrade -y`

go to your home directory

`cd ~`

Install ansible

`sudo yum install ansible`

Install nano text editor

`sudo yum install nano`

Install git

`sudo yum install git`

Create a ssh key with defaults

`ssh-keygen`

Copy the key to Authorized Keys

`cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys`

Edit hosts file under /etc/ansible

`sudo nano /etc/ansible/hosts`

Copy and paste hostsexample file to the top of the hosts file

Check the main.yaml file under vars folder

Check the wp-config.php.j2 file under templates folder and update keys with the random keys fron Wordpress site




A simple compilation of Ansible roles to install WordPress Stack on Redhat

WordPress+Apache+PHP+MariaDB Deployment with required dependencies on Redhat

Playbooks deploy a simple all-in-one WordPress configuration ready to be configured after the installation.

Update the hosts file under /etc/ansible directory to include the names or URL's of the servers you want to deploy. There is one example hosts file in the repository.

Upload your private ssh key under this path: /home/opc/.ssh/"your_key" 

Set the file permissions for the key to 600 with running sudo chmod 600 ~/.ssh/id_rsa

Then run the playbook with the below command:

ansible-playbook wordpressplaybook.yml

Good luck!
