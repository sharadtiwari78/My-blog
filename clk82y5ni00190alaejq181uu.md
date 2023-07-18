---
title: "AWS Solution Architect Associate Certification"
datePublished: Tue Jul 18 2023 09:16:15 GMT+0000 (Coordinated Universal Time)
cuid: clk82y5ni00190alaejq181uu
slug: aws-solution-architect-associate-certification-1-1
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1689670474351/3fb8af81-755b-483f-ab6e-5782b05f2eec.png
tags: cloud, aws, cloud-computing, devops, aws-certified-solutions-architect-associate

---

## **Amazon Ec2 with Lab:**

### *Introduction:*

Amazon EC2 (Elastic Compute Cloud) is a web service provided by Amazon Web Services (AWS) that offers resizable compute capacity in the cloud. Here are the key points about Amazon EC2:

* Virtual Servers: EC2 allows you to launch virtual servers called instances. These instances can be customized based on your requirements, such as the choice of operating system, instance type, storage options, and networking configurations.
    
* Scalability: EC2 provides scalable compute capacity, allowing you to easily scale up or down based on your needs. You can increase or decrease the number of instances, adjust computing resources like CPU and RAM, and handle sudden traffic spikes efficiently.
    
* Instance Types: EC2 offers a wide range of instance types optimized for different use cases. Each instance type has varying combinations of CPU, memory, storage, and networking capacity, catering to specific workload requirements.
    
* Pricing Options: EC2 offers various pricing options, including On-Demand Instances (pay-as-you-go), Reserved Instances (pre-purchased capacity), and Spot Instances (bid-based pricing). This flexibility enables you to optimize costs based on your workload characteristics and budget.
    
* Storage Options: EC2 provides multiple storage options, such as Amazon Elastic Block Store (EBS) for persistent block-level storage, Amazon S3 for object storage, and instance store volumes for temporary storage.
    
* Networking and Security: EC2 instances can be placed in Virtual Private Cloud (VPC) environments, allowing you to have complete control over your network settings. You can configure security groups, and network access control lists (ACLs), and apply various security measures to protect your instances.
    
* Integration with Other AWS Services: EC2 seamlessly integrates with other AWS services, enabling you to build highly scalable and resilient architectures. You can leverage services like Amazon RDS for managed databases, Amazon S3 for storage, and Elastic Load Balancing for distributing traffic to instances.
    
* Management and Automation: EC2 provides tools for managing and automating your instances, such as AWS Management Console, AWS Command Line Interface (CLI), and APIs. These tools allow you to monitor your instances, automate deployments, and efficiently manage resources.
    

Overall, Amazon EC2 is a powerful service that allows you to run virtual servers in the cloud, providing flexibility, scalability, and control over your computing resources.

### ***EC2 sizing & configuration options:***

* Operating System (OS): Choose between Linux, Windows, or Mac OS for your EC2 instances, based on your application's compatibility and requirements.
    
* Compute power & cores (CPU): EC2 instances offer various instance types with different virtual CPU (vCPU) counts, allowing you to select the appropriate compute power for your workload.
    
* Random-access memory (RAM): EC2 instances provide different RAM capacities, ranging from gigabytes to terabytes, enabling you to choose the right amount of memory to support your application's performance.
    
* Storage space:
    
    1\. Network-attached (EBS & EFS): Utilize Amazon Elastic Block Store (EBS) for durable block-level storage and Amazon Elastic File System (EFS) for scalable and shared file storage.
    
    2\. hardware (EC2 Instance Store): Leverage the high-performance, ephemeral storage directly attached to the EC2 instance.
    
* Network card: EC2 instances come with network cards of varying speeds, determining the network performance, while a Public IP address enables direct internet connectivity for the instance.
    
* Firewall rules: Control inbound and outbound traffic using security groups, specifying protocols, ports, and IP ranges to ensure secure access to EC2 instances.
    
* Bootstrap script (EC2 User Data): Configure your instance at launch with a bootstrap script using EC2 User Data, automating actions such as software installation and custom configurations for streamlined and consistent deployments.
    

### **EC2 User Data:**

EC2 User Data allows us to bootstrap instances by executing scripts during startup. Bootstrapping involves running commands when a machine starts, and the User Data script runs only once during the initial instance launch. It enables automating tasks like installing updates, software, and downloading files. The script has root user privileges, granting necessary permissions for executing desired actions and configurations during instance initialization. It provides flexibility to customize and automate various setup tasks to streamline deployments and ensure consistent configurations across instances.

### **EC2 Instance Types - Overview:**

* You can use different types of EC2 instances that are optimized for different use cases. [https://aws.amazon.com/ec2/instance-types](https://aws.amazon.com/ec2/instance-types/)
    
* AWS follows a consistent naming convention for its EC2 instances, such as <mark>"m5.2xlarge"</mark>. The naming convention provides key information about the instance:
    
    * "m" indicates the instance class, representing a balance between compute, memory, and networking resources.
        
    * "5" denotes the generation of the instance type, with newer generations often offering improved performance and features.
        
    * "2xlarge" represents the size within the instance class, indicating the specific configuration and capacity of the instance.
        

### EC2 Instance Types – General Purpose:

* Ideal for diverse workloads like web servers or code repositories.
    
* Provides a balanced combination of computing power, memory, and networking capabilities.
    
* The t2.micro instance, which we will be using in the course, falls under the General Purpose EC2 instance category.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689670864646/8f8a1a37-f877-46ed-b54c-ef10efaf8072.jpeg align="center")
    

### **EC2 Instance Types – Compute Optimized:**

* Designed for compute-intensive tasks demanding high-performance processors.
    
* Ideal for batch processing, media transcoding, high-performance web servers, HPC, scientific modeling, machine learning, and dedicated gaming servers.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689611842268/75ef4fd3-6a44-484f-b3dc-5a8a4a141b3b.jpeg align="center")
    

### **EC2 Instance Types – Memory Optimized:**

* Offers fast performance for workloads that require processing large datasets in memory.
    
* Well-suited for high-performance relational/non-relational databases, distributed web scale cache stores, in-memory databases optimized for BI, and real-time processing of big unstructured data.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689670935671/e9315ea9-644e-44e8-b827-a47a0358e19f.jpeg align="center")
    

### **EC2 Instance Types – Storage Optimized**

* Designed for storage-intensive tasks with high, sequential read and write access to large datasets on local storage.
    
* Well-suited for use cases like high-frequency online transaction processing (OLTP) systems, relational and NoSQL databases, cache for in-memory databases (e.g., Redis), data warehousing applications, and distributed file systems.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689612373709/ddba12b2-16a6-4dec-b7e0-a497bb9c1307.jpeg align="center")
    

### **EC2 Instance Types: example:**

![t2.micro is part of the AWS free tier (up to 750 hours per month)](https://cdn.hashnode.com/res/hashnode/image/upload/v1689612658920/c2958c50-d63e-45ec-962e-b2658a1ff450.jpeg align="center")

Great website: [click here](https://instances.vantage.sh/)

### **Introduction to Security Groups:**

* Security Groups are a foundational component of network security in AWS.
    
* They regulate inbound and outbound traffic for EC2 instances, controlling access to and from the instances.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689655939938/8bd34fa5-7097-409d-9e85-5a8e638401ea.jpeg align="center")
    
* Security groups consist of <mark>allow</mark> rules, specifying which traffic is permitted.
    
* Rules within security groups can reference IP addresses or other security groups, providing flexibility in defining access controls.
    

### **Security Groups Deeper Dive:**

* Security groups are acting as a “firewall” on EC2 instances
    
* They regulate:
    
    • Access to Ports: Security groups allow you to specify which ports on an EC2 instance are open and accessible to incoming traffic. You can define rules to permit or deny access to specific ports based on your requirements. For example, you may choose to allow incoming HTTP traffic on port 80 or SSH traffic on port 22.
    
    • Authorized IP Ranges (IPv4 and IPv6): You can configure security group rules to restrict access based on the source IP address or IP range. This provides a way to control which IP addresses are allowed to communicate with your EC2 instances. You can define both IPv4 and IPv6 addresses/ranges in security group rules.
    
    • Inbound Network Control: Security groups enable you to manage inbound network traffic that is directed toward your EC2 instances. By defining rules, you can allow incoming connections based on the protocol (such as TCP, UDP, ICMP), port numbers, and source IP addresses or IP ranges. These rules determine which incoming network traffic is permitted to reach your instances.
    
    • Outbound Network Control: Similarly, security groups also allow you to control outbound network traffic originating from your EC2 instances. You can specify rules to authorize or block outgoing connections based on the protocol, port numbers, and destination IP addresses or IP ranges. These rules dictate which outbound traffic is allowed to leave your instances.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689656655150/1aeb1345-b955-4666-ab6d-e74ec367ba13.jpeg align="center")
    

### **Security Groups Diagram:**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689656868392/63b1acb6-3c05-47af-9434-39c143df18b0.jpeg align="center")

### **Security Groups Good to know**:

* Attachable to Multiple Instances: You can associate a security group with multiple EC2 instances, allowing you to apply the same set of rules to those instances.
    
* Region/VPC Combination: Security groups are specific to a region and a virtual private cloud (VPC). They cannot be applied to instances in different regions or VPCs.
    
* Security Group's Location: Although security groups are associated with EC2 instances, they function at the network interface level. If traffic is blocked by a security group, the EC2 instance won't receive or perceive that traffic.
    
* Separate Security Group for SSH Access: It is recommended to maintain a separate security group specifically for SSH access to enhance security. This allows you to control SSH traffic separately from other types of traffic.
    
* Timeout Issues: If your application is not accessible and times out, it could be due to a misconfiguration or restriction in the security group rules.
    
* "Connection Refused" Errors: If your application returns a "connection refused" error, it typically indicates that the application itself is not running or not launched correctly, rather than a security group issue.
    
* Default Inbound and Outbound Traffic: <mark>By default, all inbound traffic is blocked</mark>, which means you need to explicitly define the rules to allow incoming connections. On the other hand, all outbound traffic is authorized by default, meaning instances can communicate with external resources unless explicitly blocked.
    

### **Referencing other security groups Diagram:**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689660075816/d58db414-330a-429c-ac6c-b2e675efe885.jpeg align="center")

### **Classic Ports to Know:**

* Port 22: Used for SSH (Secure Shell) to log into a Linux instance securely.
    
* Port 21: Used for FTP (File Transfer Protocol) to upload files into a file share.
    
* Port 22: Used for SFTP (Secure File Transfer Protocol) to upload files using SSH.
    
* Port 80: Used for HTTP to access unsecured websites.
    
* Port 443: Used for HTTPS to access secured websites.
    
* Port 3389: Used for RDP (Remote Desktop Protocol) to log into a Windows instance remotely.
    

### **Create an EC2 instance using the AWS Management Console:**

1. Sign in to the AWS Management Console.
    
    [![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689660839602/88d58885-d039-4919-910a-62cc63aea66b.jpeg align="center")](https://aws.amazon.com/console/)
    
2. Open the EC2 Dashboard.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689663584502/4114d396-1d57-4982-b069-0381cc4f01f8.jpeg align="center")
    
3. Click on the "Launch Instance" button.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689663440048/05447030-8007-49b6-bc53-bcb2949b69ea.jpeg align="center")
    
4. Choose an Amazon Machine Image (AMI) that suits your requirements. This includes selecting the operating system and pre-installed software.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689665201002/f6c8fdfe-5542-478a-be61-ba7045d76d27.jpeg align="center")
    
5. Select an instance type that matches your needs in terms of compute power, memory, and storage.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689665444630/848ac5ea-3b4e-4729-84b4-a989f3c0a4a8.jpeg align="center")
    
6. Choose an existing key pair or create a new one for SSH access.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689666934287/5636f21b-56af-40e5-aed0-209d8124bdf2.jpeg align="center")
    
7. Configure the instance details such as the network settings, subnet, and security group.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689665814935/34f5c6e4-bf90-4153-a65a-9bf9d65e015d.jpeg align="center")
    
8. (Optional) Add storage volumes to the instance.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689666019581/b6797b7d-8449-4624-9910-c8af5ac61e5e.jpeg align="center")
    
9. Scroll down to the "Advanced Details" section.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689666233395/3ba5ac5f-e3ca-4212-b23a-6320e2bba99c.jpeg align="center")
    
10. In the "User data" field, enter the script or commands you want to run on the instance at launch. This can be used for automated configuration and setup.
    
    ```plaintext
    #!/bin/bash
    # Update the instance
    sudo yum update -y
    # Install necessary packages
    sudo yum install -y httpd
    # Start and enable the httpd service
    sudo systemctl start httpd
    sudo systemctl enable httpd
    # Set up a custom index.html file
    echo "<h1>Hello World from $(hostname -f) in AZ</h1>" > var/www/html/index.html 
    ```
    
11. Configure the number of instances, and Review the summary.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689667237181/c4f33074-1c9e-427f-bfba-c86f1e22572a.jpeg align="center")
    
12. Click on Launch the instance.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689667394443/66fcea14-3434-490b-85a2-311141dfbe28.jpeg align="center")
    
13. Monitor the instance startup process and wait for it to be running.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689667950159/ebcba2ef-7977-4f99-9aeb-226eee88cb42.jpeg align="center")
    
14. Copy the instance Public IP and paste it into the browser.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689668247351/b110b973-51bd-4ee0-90fb-a33e042ad99c.jpeg align="center")
    
15. You will get the result of your user data script:
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689669718891/916183c1-c709-4d72-bc98-f0dba30c1e6f.jpeg align="center")
    

### **Thank you, and happy Learning!**