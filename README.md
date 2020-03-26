# rstudio_server
Instructions to install RStudio on AWS EC2
==

RStudio Server: 
=
* (https://rstudio.com/products/rstudio/download-server/redhat-centos/)
* OS: CentOS 
* Version 6.x

Server instructions:
=
#!/bin/bash

sudo yum update -y

sudo amazon-linux-extras install R3.4 -y

wget (https://download2.rstudio.org/server/centos6/x86_64/rstudio-server-rhel-1.2.5033-x86_64.rpm)

sudo yum -y install rstudio-server-rhel-1.2.5033-x86_64.rpm

sudo useradd carlos

echo carlos:FMarshal080417 | sudo chpasswd

AWS architecture:
=
* EC2 instance / Elastic IP
* Public Subnet / Route table
* VPC
* Internet Gateway 

