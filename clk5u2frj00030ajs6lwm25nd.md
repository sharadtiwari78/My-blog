---
title: "AWS global Infrastructure"
datePublished: Sun Jul 16 2023 19:32:05 GMT+0000 (Coordinated Universal Time)
cuid: clk5u2frj00030ajs6lwm25nd
slug: aws-global-infrastructure
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1689534914982/99fd1b4f-a6de-4cb8-9965-0d754a91dfd9.jpeg
tags: aws, devops, aws-certified-solutions-architect-associate, shubhamlondhe, tws

---

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text"><strong>AWS Global Infrastructure</strong></div>
</div>

[Aws region and availability zone map](https://aws.amazon.com/about-aws/global-infrastructure/regions_az/?p=ngi&loc=2)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689532529109/86b35663-f66b-46f9-a72f-ad7c69299c2e.png align="center")

### ***AWS Regions:***

AWS has the concept of a Region, which is a physical location around the world where we cluster data centers. We call each group of logical data centers an Availability Zone. Each AWS Region consists of a minimum of three, isolated, and physically separate AZs within a geographic area. Unlike other cloud providers, who often define a region as a single data center, the multiple AZ design of every AWS Region offers advantages for customers. Each AZ has independent power, cooling, and physical security and is connected via redundant, ultra-low-latency networks. AWS customers focused on high availability can design their applications to run in multiple AZs to achieve even greater fault tolerance. AWS infrastructure Regions meet the highest levels of security, compliance, and data protection.

AWS provides a more extensive global footprint than any other cloud provider, and to support its global footprint and ensure customers are served across the world, AWS opens new Regions rapidly. AWS maintains multiple geographic Regions, including Regions in North America, South America, Europe, China, Asia Pacific, South Africa, and the Middle East.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689532365936/22c8989f-ed6e-4d10-be32-d96acc9c6dc0.png align="center")

### ***Availability Zones (AZs):***

An Availability Zone (AZ) is one or more discrete data centers with redundant power, networking, and connectivity in an AWS Region. AZs give customers the ability to operate production applications and databases that are more highly available, fault-tolerant, and scalable than would be possible from a single data center. All AZs in an AWS Region are interconnected with high-bandwidth, low-latency networking, over fully redundant, dedicated metro fiber providing high-throughput, low-latency networking between AZs. All traffic between AZs is encrypted. The network performance is sufficient to accomplish synchronous replication between AZs. AZs make partitioning applications for high availability easy. If an application is partitioned across AZs, companies are better isolated and protected from issues such as power outages, lightning strikes, tornadoes, earthquakes, and more. AZs are physically separated by a meaningful distance, many kilometers, from any other AZ, although all are within 100 km (60 miles) of each other.

* Each region has many availability zones
    

(usually 3, min is 3, max is 6). Example:

* us-east-2a
    
* us-east-2b
    
* us-east-2c
    
* Each availability zone (AZ) is one or more discrete data centers with redundant power, networking, and connectivity
    
* They’re separate from each other so that they’re isolated from disasters
    
* They’re connected with high bandwidth, ultra-low latency networking
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689534755795/c6cb6271-6f7d-4a7f-aa82-71c71da4d330.jpeg align="center")
    

### ***AWS Points of Presence (Edge Locations):***

* Amazon has 400+ Points of Presence (400+ Edge Locations & 10+ Regional Caches) in 90+ cities across 40+ countries
    
* Content is delivered to end users with lower latency
    
    [![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689535253881/3d3c9769-e5b7-4f65-844d-c5f92274b3e9.jpeg align="center")](https://aws.amazon.com/cloudfront/features/)
    

### ***Conclusion:***

Understanding the infrastructure behind AWS services is crucial for optimizing performance, ensuring high availability, and designing resilient architectures. AWS regions provide geographically distributed options, while availability zones within those regions offer fault tolerance and redundancy. Data centers house the physical infrastructure, ensuring the reliability and security of AWS services. Finally, edge locations enhance content delivery and improve user experience. By leveraging this knowledge, you can make informed decisions when architecting your applications on AWS.