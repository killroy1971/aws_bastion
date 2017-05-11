AWS Bastion and Ansible Host
============================

This Ansible role will configure an AWS instance to be a bastion, or 
bastion and ansible host.

Variables
---------
These variables are set to either true or false:
* remove_rhui_repos - Remove AWS provided repositories
* add_epel_repo - Add the public EPEL 7 repository
* awscli_pip - Install AWS CLI tools via pip
* awscli_yum - Install AWS CLI tools via yum
* awscli_bunder - Install AWS CLI tools using Amazon's S3-hosted bundle 

Other variables:
* aws_private_key - Name of your project's primary AWS private key
* aws_user - The user Ansible will use for remote SSH login
* ssh_config_entries - List of ssh/config entries

Dependencies
------------
* Copy your project's primary AWS private key to the files directory

In defaults/main.yml:
* Set the aws_private_key variable to match the last step's filename
* Set the aws_user to the AWS instance's remote user, usually ec2_user
* Add or remove items from the ssh_config_entries list

License
-------
MIT

Author
------
Glenn H. Snead
