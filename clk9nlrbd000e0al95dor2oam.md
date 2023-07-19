---
title: "AWS Solution Architect Associate Certification"
datePublished: Wed Jul 19 2023 11:42:14 GMT+0000 (Coordinated Universal Time)
cuid: clk9nlrbd000e0al95dor2oam
slug: aws-solution-architect-associate-certification-1-1-1
tags: cloud, aws, devops, ssh, 90daysofdevops

---

### **How to SSH into your EC2 instance: Step-by-Step**

Linux and Mac OS

### **Introduction:**

SSH (Secure Shell) is a widely used protocol that allows you to securely connect to your Amazon Elastic Compute Cloud (EC2) instances. SSH provides a secure channel for accessing and managing your EC2 instances remotely. In this article, we will walk you through the step-by-step process of SSHing into your EC2 instance.

### **Step 1:**

**Ensure Your EC2 Instance is Running:** Before you can SSH into your EC2 instance, make sure it is in the "running" state. Log in to the AWS Management Console and navigate to the EC2 service. Check the status of your EC2 instance and ensure it is running.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689739889844/954b141e-c4f2-4baf-91db-86be30c4af13.jpeg align="center")

### **Step 2:**

**Obtain the Public IP Address or DNS Name:** To establish an SSH connection, you need the public IP address or DNS name of your EC2 instance. In the EC2 dashboard, select your instance and locate the "Public IP" or "Public DNS (IPv4)" field in the instance details.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689740894516/0b62c082-83d5-408d-86d2-c338fdcdb8b0.png align="center")

### **Step 3:**

**Set Permissions for Your Private Key File:** For security reasons, you need to restrict the permissions of your private key file. In your terminal or command prompt, navigate to the directory where the private key file is located and run the following command:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689765918271/2ebb58cc-d295-444c-a7c7-9f851291b847.jpeg align="center")

```plaintext
ls
chmod 400 your-private-key.pem
```

### **Step 4:**

**Connect to Your EC2 Instance**: In your terminal or command prompt, run the SSH command with the following syntax:

```plaintext
ssh -i your-private-key.pem ec2-user@public-ip-or-dns
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689766576349/9c759bf9-0930-4834-9cb8-4911142008c1.jpeg align="center")

### **Step 5:**

**Confirm the Connection**: If everything is set up correctly, you should now be connected to your EC2 instance via SSH. You will see a command prompt indicating a successful connection.

Example:

```plaintext
[ec2-user@ip-XX-XX-XX-XX ~]$
```

That's it! You have successfully SSHed into your EC2 instance using your existing key pair. Now you can execute commands and interact with your EC2 instance through the terminal or command prompt.

Thank you, and Happy Learning!!