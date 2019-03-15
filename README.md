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


## More details coming

#ServiceNOW
#LinuxMIDServer


