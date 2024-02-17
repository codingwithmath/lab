# Creating a EC2 in AWS with Terraform

following the terraform docs for this

https://developer.hashicorp.com/terraform/tutorials/aws-get-started/aws-build

should pay attention to the provider region, it should be like your aws-cli configuration and your aws account


- Got in trouble when trying to update de main.tf
- Somehow the credentials that I used in the first apply worked, but in the second time it didnt worked anymore...
- updated the aws credentials, using the provided CSV file and it worked
- seems like an aws bug.
- tried to access the ec2 via ssh, configuring a ssh key pair in terraform, but no success. 
- update the required_provider to version 5, trying to solve the invalid credentials problem. 
- in the version 5, terraform does not look to the exported aws variables, but de aws-cli configured ones.
- was able to destroy the ec2 with success


# Goal
- be able to access the ec2 via ssh
- be able to run a docker container and a kubernetes in the ec2

