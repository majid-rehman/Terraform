# terraform-infrastructure-as-code

## AWS Setup

Here are some notes to clarify the setup
Make sure you have installed the AWS CLI
if you use my vagrant devops-box it is included by default
otherwise you can download it manually from https://aws.amazon.com/cli/
If you're on linux you can also use "sudo pip install --upgrade awscli"
If you don't have pip, try sudo apt-get install python-pip
There is a lecture on how to add an admin user, this need to be done to create an access key and secret key
Use "aws configure" to enter the keys
you can optionally specify a default region - but no worries, in terraform you can set any region you want
Use http://www.cloudping.info/ to determine your region
You can test whether it works by entering: aws iam get-user
This will also show your AWS userid which you need afterwards
Useful Commands

$ terraform plan                                  # plan

$ terraform apply                                 # shortcut for plan & apply - avoid this in production

$ terraform plan -out out.terraform      # terraform plan and write the plan to out file

$ terraform apply out.terraform            # apply terraform plan using out file

$ terraform show                                  # show current state

$ cat terraform.tfstate                           # show state in JSON format



## Using putty instead of the ssh command

This is explained using MacOS/Linux. If you rather want to use putty, use the following steps to create your SSH keypair:

Download Putty and PuttyGen from http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html
Launch PuttyGen and click the "Generate" button to generate a new public/private key
You can enter a passphrase or leave it blank
Save the public and private keys by clicking the Save public key and Save private key buttons


Reference Documentation

- Download URL: https://www.terraform.io/downloads.html
- AWS Resources: https://www.terraform.io/docs/providers/aws/
- List of providers: https://www.terraform.io/docs/providers/index.html


# Practise overview
Practise Directory | Description
------------ | -------------
first-steps | First steps
practise-1 | First steps: Launching an EC2 instance
practise-2 | Using provisioner
practise-2b | Using provisioner on a Windows instance
practise-3 | Executing script locally
practise-4 | Outputting
practise-5 | Data Source
practise-6 | Modules
practise-7 | AWS VPC
practise-8 | EC2 instance within VPC with securitygroup
practise-9 | EC2 instance with EBS volumes
practise-10 | Userdata and cloudinit
practise-11 | Route53 (DNS)
practise-12 | RDS
practise-13 | IAM
practise-14 | IAM Roles with S3 bucket
practise-15 | Autoscaling
practise-16 | Autoscaling with ELB (Elastic Load Balancer)
practise-17 | Elastic Beanstalk PHP 7 stack with RDS
practise-18 | Interpolations, VPC module
practise-18b | Project structure, best practices
packer-practise | Build AMIs with Packer
jenkins-packer-practise | practise with jenkins and Packer
docker-practise-1 | Using ECR - The EC2 Container Registry
docker-practise-2 | Using ECS - The EC2 Container Service
docker-practise-3 | Using ECR/ECS with Jenkins in a complete workflow
module-practise | Using ECS + ALB in 4 modules to show how developing terraform modules work
