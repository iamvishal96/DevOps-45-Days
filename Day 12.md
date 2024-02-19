Day 12 Devops 
1. **Creating an IAM User and Login**:
   - Go to the AWS Management Console and navigate to the IAM service.
   - Click on "Users" in the left-hand menu, then click "Add user".
   - Enter a username, select access type (Programmatic access, AWS Management Console access, or both), and proceed.
   - Set permissions by adding the user to one or more groups with appropriate policies or attach policies directly.
   - Review and create the user. Make sure to save the user's access key ID and secret access key if creating a user with programmatic access.

2. **Creating an EC2 Instance**:
   - Go to the AWS Management Console and navigate to the EC2 service.
   - Click on "Launch Instance" to start the instance creation wizard.
   - Choose an Amazon Machine Image (AMI), select an instance type, configure instance details (e.g., network settings, storage), and add tags for identification.
   - Configure security groups to control inbound and outbound traffic to the instance.
   - Review and launch the instance. Make sure to select or create a key pair for SSH access if you plan to connect via SSH.

   Best practices:
   - Always use the latest generation of instance types for better performance and cost-effectiveness.
   - Regularly update and patch your instances to protect against security vulnerabilities.
   - Utilize AWS IAM roles for instances to securely grant permissions to AWS resources.
   - Enable detailed monitoring for better visibility into instance performance.

3. **Accessing the EC2 Instance**:
   - Once the instance is running, you can connect to it via SSH (for Linux instances) or RDP (for Windows instances) using the key pair or password provided during instance creation.
   - Use the public DNS or public IP address of the instance along with the appropriate credentials to connect.

4. **Deploying an Application on AWS EC2**:
   - Connect to your EC2 instance.
   - Install any necessary software dependencies for your application.
   - Upload your application code to the instance.
   - Configure your application to run on the instance, setting up any required environment variables or configuration files.
   - Start your application.

5. **Exposing the Application to the Outside World**:
   - Configure security groups to allow inbound traffic on the necessary ports for your application.
   - Assign an Elastic IP (EIP) to your instance for a static public IP address, if needed.
   - Update DNS records if you're using a custom domain.

6. **Accessing the Application Deployed on AWS from Your Laptop**:
   - Use the public DNS or IP address of your EC2 instance to access the application deployed on AWS from your laptop's web browser or terminal.
