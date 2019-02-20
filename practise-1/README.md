# practise-1

```
vagrant ssh
```
###### Checking Terraform is installed corectly
```
terraform  > to check terraform is working
```
###### Checking git is installed 
```
git     > to check git is installed 
```
###### Clone the terraform repository here 
```
git clone https://github.com/majidkhan138/Terraform.git
```
###### cd to terraform and than to every module you want to use
```
cd terraform && cd practise-1
```

* Initialize terraform
```
terraform init
```

###### Now ls the repo and than try on `terraform apply`
```
terraform apply
```
* If it works it will ask for the AWS_ACCESS_KEY , SECRET_KEY etc ..
- Because i didn't provide my credentials
- Create terraform.tfvars to give your crendentials as a variable for security
```
vim terraform.tfvars
```
 > to exit from vim type `:wq!`

* Add your credentials like that but remember to put this file in .gitignore so it will not uplaod to git repo ..
```
AWS_ACCESS_KEY = " enter here "
AWS_SECRET_KEY = " enter here "
AWS_REGION = " enter here "
```
###### There is still chance of error , request is invalid similar to that ..
* it's because of date differene in your local system and on vagrant
```
date
```
* Check if it is correct , debug the error if not run this command
```
sudo apt-get install ntpdate; sudo ntpdate ntp.ubuntu.com
```
* Now run terraform apply
```
terraform apply
```

