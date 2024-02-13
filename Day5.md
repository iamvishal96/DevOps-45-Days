## DAY 5 
### AWS CLI (Command Line Interface)
The AWS Command Line Interface (CLI) is a unified tool to manage AWS services through the command line. It provides users with direct access to various AWS services and allows for scripting and automation of tasks.

Here are some key points about the AWS CLI:

1. **Installation**: You can install the AWS CLI on your laptop by downloading and installing the appropriate package for your operating system. You can find installation instructions in the [AWS CLI documentation](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html).

2. **Configuration**: After installation, you need to configure the AWS CLI with your AWS credentials. This includes your Access Key ID and Secret Access Key. You can configure the CLI using the `aws configure` command and providing the required information.

3. **Usage**: Once configured, you can start using the AWS CLI to interact with AWS services. You can run commands to manage EC2 instances, S3 buckets, IAM users, and more. For example, you can list EC2 instances using `aws ec2 describe-instances` or create new EC2 instances using `aws ec2 run-instances`.

### Connecting to EC2 Instance

There are several ways to connect to an EC2 instance from your laptop and console:

1. **SSH**: If the EC2 instance is running a Linux-based operating system, you can connect to it using SSH (Secure Shell). You need the public IP address or DNS name of the instance and the private key associated with the instance. The command to connect typically looks like this:
   
   ```
   ssh -i /path/to/private/key.pem username@public-ip-address
   ```

2. **RDP**: If the EC2 instance is running Windows, you can connect to it using Remote Desktop Protocol (RDP). You need the public IP address or DNS name of the instance and the administrator username and password set during instance creation.

### AWS CloudFormation (CFT)

AWS CloudFormation is a service that allows you to define and provision AWS infrastructure as code. Instead of manually creating and configuring AWS resources, you can use CloudFormation templates to describe the desired state of your infrastructure. CloudFormation then handles the creation, update, and deletion of resources in a safe and predictable manner.

Key points about AWS CloudFormation:

1. **Templates**: CloudFormation templates are JSON or YAML files that describe the AWS resources and their configurations. Templates can include parameters, mappings, conditions, resources, and outputs.

2. **Stacks**: Templates are used to create stacks, which are collections of AWS resources provisioned and managed together as a single unit. Stacks can be created, updated, and deleted as a whole.

3. **Automation**: CloudFormation enables infrastructure as code practices, allowing you to version control your infrastructure, replicate environments easily, and automate deployments.

4. **Integration**: CloudFormation integrates with other AWS services such as AWS Lambda, AWS CloudTrail, and AWS Config for enhanced functionality and monitoring.

By using CloudFormation, you can ensure consistency, reliability, and scalability of your AWS infrastructure deployments.
