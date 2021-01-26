
# GiffGaff
This Repository is created for AWS Infrastructure using Terraform

# Terraform
Connecting to a AWS Instance in a private subnet

Steps:

To get started clone the repo:

Clone the repository

The next step is to generate the SSH keys. 
In the terraform directory create another directory called keys and create your keys with the following command:
# create the keys
ssh-keygen -f mykeypair

##SSH Config File:

Host bastion-instance
   HostName <Bastion Public IP>
  

Host private-instance
   HostName <Private IP>a
   ProxyCommand ssh -q -W %h:%p bastion-instance

