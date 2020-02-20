# infrastructure
This JSON is as a cloud formation template 

## Prerequisit 
AWS CLI set up on local machine 
reference : https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html

## Execution Steps
1. To create Cloud formation Stack
 aws cloudformation create-stack \
  --stack-name csye6225demo \
  --parameters ParameterKey=InstanceTypeParameter,ParameterValue=value \
  --template-body file://networking.json

2. To Delete Cloud formation Stack
aws cloudformation delete-stack --stack-name csye6225demo 

 ## Variables provided in CLI
 Template Name
 AWS Region
 VPC Name
 VPC CIDR
 Subnet1 CIDER
 subnet2 CIDER
 subnet3 CIDER
 name of the JSON file 

 ## Networking setup
 1. Create a VPC(vpc)
 2. Three subnets created in the VPC
 3. Internet gateway, along with Internet gatewayVPC attachment
 4. Public Route table along with all the subnets attached to this table 
 5. Public Route in the public Router table with destination CIDR block 0.0.0.0/0 and internet gateway created as target.

 