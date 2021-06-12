# Project: To create following resources on AWS

1. new VPC
2. new Subnet
3. New Security Group
   - source: 0.0.0.0/0
   - ports: 443, 80, 22
4. New ec2 instance
   - install Nginx webserver

download the files and perform following actions:
Save AWS credentials on sevrets.yml file and encrypt it.

    ansible-vault encrypt secrets.yml

Commands:
1. By default script will only get ec2 information

        ansible-playbook practice.yml --ask-vault-pass
    
2. To create VPC and Create-ec2 run playbook with tags: create-vpc, create-ec2

        ansible-playbook practice.yml --ask-vault-pass --tags=create-vpc,create-ec2
