---
title: "AWS Solution Architect Associate Certification"
datePublished: Thu Jul 20 2023 14:20:57 GMT+0000 (Coordinated Universal Time)
cuid: clkb8pphj001d09kuewxtcict
slug: aws-solution-architect-associate-certification-1-1-1-1
tags: aws, cloud-computing, aws-certified-solutions-architect-associate, 90daysofdevops, ec2-connect

---

### EC2 Instance Connect

### **Introduction:**

Amazon Web Services (AWS) offers a plethora of services that empower businesses to build, deploy, and manage applications in the cloud. Among its numerous offerings, AWS EC2 (Elastic Compute Cloud) stands out as a popular service for launching virtual servers in the cloud. To enhance the security and ease of managing EC2 instances, AWS introduced EC2 Instance Connect, a secure and seamless way to access instances using SSH directly from the AWS Management Console.

### **What is EC2 Instance Connect?**

you are traditionally, accessing an EC2 instance required generating and managing SSH key pairs manually, which could be cumbersome and prone to security risks. EC2 Instance Connect simplifies this process by enabling you to access your EC2 instances securely using the AWS Management Console, without the need to handle SSH key pairs manually.

### **Benefits of EC2 Instance Connect:**

1. Enhanced Security: EC2 Instance Connect eliminates the need for users to manage SSH keys manually. This reduces the risk of key theft, and unauthorized access, and ensures that only authorized users with proper IAM permissions can access the instances.
    
2. Simplified Access Management: IAM roles provide a robust framework for controlling user access. Administrators can easily grant or revoke permissions to specific instances, streamlining the access management process.
    
3. Auditability: All EC2 Instance Connect activity is logged by AWS CloudTrail, allowing for easy auditing and monitoring of access events. This feature improves traceability and helps meet compliance requirements.
    
4. Easy to Use: EC2 Instance Connect streamlines connecting to instances through the AWS Management Console. Users no longer need to maintain SSH keys or use third-party tools to access their instances.
    
5. Multi-Account Access: EC2 Instance Connect can be used across multiple AWS accounts. This is particularly useful for organizations that operate under an AWS multi-account strategy.
    

### **Good to know:**

1. No need to use your key file that was downloaded
    
2. The “magic” is that a temporary key is uploaded onto EC2 by AWS
    
3. Works only out-of-the-box with Amazon Linux 2
    
4. Need to make sure port 22 is still open!
    

### **EC2 Instances Purchasing Options:**

* On-Demand Instances offer predictable pricing, pay per second, perfect for short workloads with flexibility.
    
* Reserved Instances provide cost savings for long workloads with 1 or 3-year commitments.
    
* Convertible Reserved Instances offer the same savings with the flexibility to change instance types.
    
* Savings Plans offer cost benefits for long workloads, allowing commitment to a specific usage amount.
    
* Spot Instances are cost-effective but less reliable, suitable for short workloads.
    
* Dedicated Hosts give control over instance placement by booking an entire physical server.
    
* Dedicated Instances ensure exclusive hardware usage without sharing with other customers.
    
* Capacity Reservations let you reserve capacity in a specific Availability Zone for any duration.
    

### **EC2 On Demand:**

* EC2 On-Demand charges you based on actual usage, making it pay-as-you-go.
    
* Linux/Windows billed per second after the first minute, while other OS billed per hour.
    
* No upfront payment, but the highest cost compared to other options.
    
* Enjoy flexibility with no long-term commitment requirements.
    
* Ideal for unpredictable workloads and short-term usage scenarios.
    

### **EC2 Reserved Instances:**

* EC2 Reserved Instances offer up to 72% savings compared to On-Demand pricing.
    
* Reserve specific attributes: Instance Type, Region, Tenancy, and OS.
    
* Reservation Period – 1 year (+discount) or 3 years (+++discount)
    
* Payment Options – No Upfront (+), Partial Upfront (++), All Upfront (+++)
    
* Reserved Instances can be scoped regionally or zonally for AZ-specific capacity reservation.
    
* Ideal for steady-state usage applications like databases.
    
* Utilize the Reserved Instance Marketplace to buy and sell reservations.
    
* Convertible Reserved Instances offer up to 66% discount and allow changes to instance attributes.
    
* Modify EC2 instance type, family, OS, scope, and tenancy with Convertible Reserved Instances.
    

### EC2 Savings Plans:

* EC2 Savings Plans offer up to 72% discount, like Reserved Instances (RIs), for long-term usage commitment.
    
* Commit to a specific usage amount, e.g., $10/hour, for 1 or 3 years.
    
* Any usage beyond Savings Plans is billed at the regular On-Demand price.
    
* Savings Plans are bound to a specific instance family and AWS region, e.g., M5 in us-east-1.
    
* Flexibility across instance sizes, such as m5.xlarge and m5.2xlarge, within the chosen family and region.
    
* Tenancy options: Host, Dedicated, and Default.
    

### **EC2 Spot Instances**

* Can get a discount of up to 90% compared to On-demand
    
* Instances that you can “lose” at any point of time if your max price is less than the current spot price
    
* The MOST cost-efficient instances in AWS
    
* Useful for workloads that are resilient to failure
    
    • Batch jobs
    
    • Data analysis
    
    • Image processing
    
    • Any distributed workloads
    
    • Workloads with a flexible start and end time
    
* Not suitable for critical jobs or databases
    

### **EC2 Dedicated Hosts:**

* EC2 Dedicated Hosts offer fully dedicated physical servers for your exclusive use.
    
* Ideal for addressing compliance requirements and utilizing existing server-bound software licenses.
    
* Choose between On-Demand or Reserved options with various payment plans.
    
* While the most expensive, Dedicated Hosts ensure complete isolation for sensitive workloads.
    
* Suitable for complex licensing models like BYOL (Bring Your Own License).
    
* Perfect for companies with stringent regulatory or compliance requirements.
    

### **EC2 Dedicated Instances:**

1. EC2 Dedicated Instances run on hardware exclusively dedicated to your account.
    
2. While dedicated, they may share hardware with other instances within your account.
    
3. You have no control over instance placement, as hardware can be moved after stopping and starting.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689857686008/3bde0afd-4500-4809-9b0e-9f3cefa111b9.jpeg align="center")
    

### **EC2 Capacity Reservations:**

1. Reserve On-Demand instance capacity in a specific Availability Zone (AZ) for any duration.
    
2. Always have access to the reserved capacity whenever you need it.
    
3. Create and cancel reservations anytime without a time commitment or billing discounts.
    
4. Combine with Regional Reserved Instances and Savings Plans to maximize billing discounts.
    
5. Charged at the On-Demand rate regardless of whether you run instances or not.
    
6. Ideal for short-term, uninterrupted workloads requiring a specific AZ presence.
    

### **Which purchasing option is right for me?**

* **On-Demand:** Ideal for spontaneous stays, pay the full price per room without any long-term commitment.
    
* **Reserved:** Perfect for planned, extended stays, securing a discount by committing to a specific duration.
    
* **Savings Plans:** Pay a fixed amount per hour for a certain period, offering flexibility to choose room types.
    
* **Spot Instances:** Similar to last-minute deals, bid for empty rooms and stay at a lower cost, but you may get kicked out.
    
* **Dedicated Hosts:** Book an entire building, ensuring complete isolation and control over resources during your stay.
    
* **Capacity Reservations:** Reserve a room for a period, paying the full price even if you don't stay in it, providing assurance of availability.
    

### **Price Comparison**

**Example – m4.large – us-east-1**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689859687052/530352c6-e3f0-4b84-8b15-52936581e62a.jpeg align="center")

### EC2 Spot Instance Requests:

* Can get a discount of up to 90% compared to On-demand
    
* Define max spot price and get the instance while the current spot price &lt; max
    
    • The hourly spot price varies based on offer and capacity
    
    • If the current spot price &gt; your max price you can choose to stop or terminate your instance with a 2 minutes grace period.
    
* Other strategy: Spot Block
    
    • “block” spot instance during a specified time frame (1 to 6 hours) without interruptions
    
    • In rare situations, the instance may be reclaimed
    

• **Used for batch jobs, data analysis, or workloads that are resilient to failures.**

• **Not great for critical jobs or databases**

### EC2 Spot Instances Pricing:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689860412439/20c001c8-d611-4b11-b8d3-77d6f59a23e8.jpeg align="center")

[click here](https://us-east-2.console.aws.amazon.com/ec2/home?region=us-east-2#)

### **Spot Fleets:**

* Spot Fleets = set of Spot Instances + (optional) On-Demand Instances
    
* The Spot Fleet will try to meet the target capacity with price constraints
    
    • Define possible launch pools: instance type (m5.large), OS, Availability Zone
    
    • Can have multiple launch pools, so that the fleet can choose
    
    • Spot Fleet stops launching instances when reaching capacity or max cost
    
* Strategies to allocate Spot Instances:
    
    • **lowest price:** from the pool with the lowest price (cost optimization, short workload)
    
    • **diversified:** distributed across all pools (great for availability, long workloads)
    
    • **capacity-optimized:** pool with the optimal capacity for the number of instances
    
    • **priceCapacityOptimized (recommended):** pools with the highest capacity available, then select the pool with the lowest price (best choice for most workloads)
    
* Spot Fleets allow us to automatically request Spot Instances with the lowest price