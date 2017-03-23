# Overview
This project creates an [Amazon Machine Image](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html) with
[Logstash](https://www.elastic.co/products/logstash) pre-installed and ready to be connected to
[Amazon Elasticsearch Service](https://aws.amazon.com/elasticsearch-service/).

# Prerequisites
* a working [Packer](https://www.packer.io/) installation
* a working [Ansible](https://www.ansible.com/) installation
* a working [Bash](https://www.gnu.org/software/bash/) installation
* your AWS IAM keys exported to the environment
    * AWS_ACCESS_KEY_ID
    * AWS_SECRET_ACCESS_KEY
    * AWS_REGION

Testing was done under Ubuntu 16.04 Linux.

# Building

Typing `./build.sh` will run Packer and build out an AMI image which can be used in
[CloudFormation](https://aws.amazon.com/cloudformation/) templates.

Configurable values are located in `variables.json`.  You may edit these as need to customize the template.

# Installation

Other than the prerequisites, there is nothing to install.  The script will install into the region's AMI registry.

# Tips and Tricks

## Ansible Roles
The playbook reuses logic from [open source Ansible roles](https://galaxy.ansible.com/kurron/). Consult those
playbooks to learn exactly how certain aspects of the plays are configured.

# Troubleshooting

# License and Credits
This project is licensed under the [Apache License Version 2.0, January 2004](http://www.apache.org/licenses/).
