AWS EC2 Deployment with Terraform
Project Objective

* Understand AWS core concepts.
* Launch an EC2 instance manually through the AWS Console.
* Automate EC2 deployment using Terraform.
* Document the entire process for reference.

[1] Understand AWS Core Concepts

Before deploying EC2, the following AWS fundamentals were studied:

1. What is AWS

* AWS (Amazon Web Services) is a cloud computing platform.
* Provides services like servers, storage, databases, networking, security, etc.
* Pay-as-you-go model (you pay only for what you use).

2. Regions and Availability Zones

* Region = Physical geographic location (e.g., Mumbai, US East).
* Availability Zone (AZ) = Multiple data centers inside a region.
* Used for high availability and fault tolerance.

3. EC2 (Elastic Compute Cloud)

* Virtual server in the cloud.
* Used to run applications, websites, or software.
* You can choose OS, CPU, RAM, and storage size.

4. IAM (Identity and Access Management)

* Manages users, roles, and permissions.
* Provides secure access control to AWS resources.
* Follows least privilege principle (give only required access).

5. VPC (Virtual Private Cloud)

* A private network inside AWS.
* Controls IP ranges, subnets, routing, and internet access.
* Improves security and network isolation.

6. Security Groups

* Acts like a virtual firewall for EC2.
* Controls inbound and outbound traffic (ports like 22 for SSH, 80 for HTTP).

7. Key Pairs

* Used for secure login into EC2 instances.
* Consists of public key (AWS) and private key (user).
* Required for SSH access.

8. Storage (EBS)

* Elastic Block Store is a virtual hard disk attached to EC2.

* Stores OS, files, and application data.

[2]. Launch an EC2 Instance Manually through AWS Console

Step 1 – Login to AWS Console

* Open https://aws.amazon.com
* Sign in using AWS account credentials.
* Navigate to EC2 Dashboard from Services.

Step 2 – Choose Region

* Select a Region (example: Asia Pacific – Mumbai).

Step 3 – Launch Instance

* Click Launch Instance button.
* Provide an Instance Name.

Step 4 – Select AMI (Amazon Machine Image)

* Choose an OS template.
* AMI contains OS and pre-installed software.

Step 5 – Choose Instance Type

* Selected t2.micro (Free Tier eligible).
* Defines CPU, RAM, and performance.

Step 6 – Create / Select Key Pair

* Created a new key pair (RSA / .pem).
* Downloaded private key securely.
* Used for SSH login into EC2.

Step 7 – Configure Network Settings

* Used default VPC.
* Enabled Auto-assign Public IP.
* Created a Security Group:
* SSH – Port 22 

Step 8 – Review and Launch

* Reviewed all configurations.
* Clicked Launch Instance.

Step 9 – Connect to Instance

* Waited until Instance State = Running.
* Copied Public IPv4 Address.

=> Connected using SSH:
ssh -i key.pem ec2-user@public-ip