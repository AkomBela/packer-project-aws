This project uses Packer to create an Amazon Machine Image (AMI) on AWS. The AMI is based on Ubuntu 20.04 (Focal) and includes pre-installed software, such as Redis.

Prerequisites
Packer: Ensure you have Packer installed on your local machine.
AWS CLI: Configure your AWS credentials using the AWS CLI or set the appropriate environment variables (AWS_ACCESS_KEY_ID, AWS_SECRET_ACCESS_KEY).
HashiCorp Vagrant: Used for post-processing (if necessary).
Project Structure
aws-ubuntu.pkr.hcl: The main Packer configuration file defining the AWS AMI build process.
variables.pkr.hcl: Contains variables used within the Packer configuration.
Packer Configuration
required_plugins
Variables
ami_prefix: Prefix for the AMI name. Default: "learn-packer-linux-aws-redis"
timestamp: Automatically generated timestamp for creating unique AMI names.
Usage
Clone the Repository:

bash
Copy code
git clone https://github.com/your-username/packer-aws-ubuntu-focal.git
cd packer-aws-ubuntu-focal
Install Packer:

If Packer is not installed, follow the instructions here to install it.

Configure AWS Credentials:

Ensure your AWS credentials are set up, either through the AWS CLI or by setting environment variables.

Build the AMI:

Run the following command to build the AMI:

bash
Copy code
packer build aws-ubuntu.pkr.hcl
Verify the Build:

After the build completes, check your AWS Management Console to verify that the AMI was created successfully.
