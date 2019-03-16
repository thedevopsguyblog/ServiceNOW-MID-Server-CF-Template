# ServiceNOW MID Server Deployment - AWS Cloudformation Templates
This repo contains two cloudformation templates.

The "CFTemplate.yml" will deploy a VPC, 3 Subnets, a Linix AMI and all other associated infrastructure.
The "EC2Instance-CFtemplate.yml" will deploy just a Amazon Linux AMI an S3 bucket.

For further details read the templates. 

What will it be, red pill or blue? :)


## Introduction
This repo contains an AWS Cloudformation template that will deploy a Centos 7.x AMI(T2micro) to a public VPC with the SNWO MID server deployed.

What you need to do...
- Upload the MID server as a .zip to the S3 bucket, chnage the name of the bucket in the CF template (also update the "Userdata" section)
- On the EC2 instance edit the config.xml file "/SNOW/MID/agent/config.xml" to include your SNOW details. 
- start the MID server by running: "/SNOW/MID/agent/start.sh"

Errors?

Check the "/SNOW/MID/agent/logs" directory.


#ServiceNOW
#LinuxMIDServer


