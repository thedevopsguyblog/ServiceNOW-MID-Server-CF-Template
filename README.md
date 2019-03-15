# Install and Configure ServiceNOW MID AWS Cloudformation Template
ServiceNow MID server deployed and installed using AWS CloudFormation 

NOTE: This was all tested on the London instace of SNOW.

## Introduction
This repo contains an AWS Cloudformation template that will deploy a Centos 7.x AMI(T2micro) to a public VPC with the SNWO MID server deployed.

What you need to do...
- Upload the MID server install package as a .zip to an S3 bucket, chnage the name of the bucket in the CF template.
- On the EC2 instance edit the config.xml file "/SNOW/MID/agent/config.xml" to include your SNOW details. 
- start the MID server by running: "/SNOW/MID/agent/start.sh"

Errors?

Check the "/SNOW/MID/agent/logs" directory.


## The CF Template Explained

If you want to deploy JUST the MID server, use the template "EC2Instance-CFtemplate", other wise if you want to deploy the entire environemnt use "CFTemplate"

Full Template will deploy the follwoing 
- 1x Public VPC with 3x Subnets, Auto assign public IP = True(with an IGW, DHC, ACL and Route table all configured)
- 1x EC2 Instance and 1x Security Group (Inbound = Allow 0.0.0.0/0 Outboud = Allow 0.0.0.0/0)
- 1x S3 Bucket (NOTE: Put the .zip MID install in here)



#ServiceNOW
#LinuxMIDServer


