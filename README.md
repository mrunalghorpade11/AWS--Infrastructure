# infrastructure
This JSON is as a cloud formation template 

##Prerequisit 
AWS CLI set up on local machine 
reference : https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html

## Execution Steps
 aws cloudformation create-stack --stack-name csye6225T --parameters ParameterKey=awsRegion,ParameterValue=us-east-2 ParameterKey=VpcName,ParameterValue=myVpc1 ParameterKey=VpcCIDR,ParameterValue=10.0.0.0/16 ParameterKey=SubnetCIDR1,ParameterValue=10.0.10.0/24 ParameterKey=SubnetCIDR2,ParameterValue=10.0.11.0/24 ParameterKey=SubnetCIDR3,ParameterValue=10.0.12.0/24 --template-body file://networking.json --profile dev
 
 ##Variables provided in CLI
 Template Name
 AWS Region
 VPC Name
 VPC CIDR
 Subnet1 CIDER
 subnet2 CIDER
 subnet3 CIDER
 name of the JSON file 

 ##Networking setup
 1. Create a VPC(vpc)
 2. Three subnets created in the VPC
 3. Internet gateway, along with Internet gatewayVPC attachment
 4. Public Route table along with all the subnets attached to this table 
 5. Public Route in the public Router table with destination CIDR block 0.0.0.0/0 and internet gateway created as target.

 