# first-step 

# Quickly Configuring the AWS CLI
```
$ aws configure
AWS Access Key ID [None]: AKIAIOSFODNN7EXAMPLE
AWS Secret Access Key [None]: wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
Default region name [None]: us-west-2
Default output format [None]: json
```

###### Add your credentials directly in `instance.tf` , But it is not good due to security reasons
* For local practise only , don't push this module with your credentials

###### Remember to set the date as it as in your local system
```
$sudo apt-get install ntpdate; sudo ntpdate ntp.ubuntu.com
```

```
$terraform apply
```