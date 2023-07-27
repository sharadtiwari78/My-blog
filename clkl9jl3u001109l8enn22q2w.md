---
title: "AWS Solution Architect Associate Certification"
datePublished: Thu Jul 27 2023 14:41:52 GMT+0000 (Coordinated Universal Time)
cuid: clkl9jl3u001109l8enn22q2w
slug: aws-solution-architect-associate-certification-1-1-1-1-1
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1690468348124/15604612-1ea0-4950-bc36-c626f2514c1e.png
tags: aws, aws-certified-solutions-architect-associate, aws-community, tws, priavte-vs-public-ip

---

### **Private vs Public IP (IPv4)**

* Networking has two IP types: IPv4 and IPv6, the former being widely used online.
    
* IPv4 addresses consist of four sets, e.g., 1.160.10.240, enabling 3.7 billion public addresses.
    
* IPv4's format: \[0-255\].\[0-255\].\[0-255\].\[0-255\], providing a wide range of public addresses.
    
* IPv6 offers enhanced security and scalability compared to the traditional IPv4.
    
* IPv4 still plays a crucial role due to its widespread adoption and compatibility.
    
* Public IP addresses are unique and identifiable on the internet.
    
* Private IP addresses are used within local networks, like 192.168.0.1.
    
* Private IPs offer internal communication and are not directly accessible from the internet.
    
* Private IPs are often assigned by routers using Dynamic Host Configuration Protocol (DHCP).
    

### **Private vs Public IP (IPv4) Example**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690463721157/49b0e0e9-be98-4e96-bf2b-406502ea42af.jpeg align="center")

### **Private vs Public IP (IPv4) Fundamental Differences**

**Private IP (IPv4):**

* Used within local networks to facilitate communication among devices.
    
* Private IPs are non-routable on the internet and provide internal network addressing.
    
* Common private IP address ranges include 192.168.0.0 - 192.168.255.255, 10.0.0.0 - 10.255.255.255, and 172.16.0.0 - 172.31.255.255.
    
* Devices with private IPs can't be accessed directly from the internet.
    
* Enables local network communication and serves as an extra layer of security.
    

**Public IP (IPv4):**

* Unique and routable addresses are used on the internet to identify devices globally.
    
* Provided by Internet Service Providers (ISPs) to individual devices for direct internet access.
    
* Allows devices to be accessed and communicated with from anywhere on the internet.
    
* Each device has a distinct public IP address.
    
* Vital for hosting web servers, running online services, and establishing direct connections
    

### **What is Elastic IP**

* Stopping and starting an EC2 instance can change its public IP; Elastic IP provides a fixed address.
    
* Elastic IP is a static public IPv4 address that you own until deletion.
    
* Attachable to one instance at a time, it helps maintain a consistent address for your instance.
    
* Elastic IP offers rapid remapping during instance or software failures, enhancing fault tolerance.
    
* AWS limits each account to 5 Elastic IPs; a request can increase this limit.
    
* Elastic IPs should be avoided, as they may indicate suboptimal architectural choices.
    
* Prefer using random public IPs and associating them with DNS names for flexibility.
    
* Alternatively, opt for Load Balancers instead of assigning a public IP to individual instances.
    

### **Placement Groups:**

* Control EC2 instance placement strategy using placement groups.
    
* Options: Cluster for low-latency group, Spread for hardware dispersion.
    
* When you create a placement group, you specify one of the following strategies for the group:
    
    1. **Cluster** \- packs instances close together inside an Availability Zone. This strategy enables workloads to achieve the low-latency network performance necessary for tightly-coupled node-to-node communication that is typical of high-performance computing (HPC) applications.
        
    2. **Spread** \- strictly places a small group of instances across distinct underlying hardware to reduce correlated failures.
        
    3. **Partition -** spreads your instances across logical partitions such that groups of instances in one partition do not share the underlying hardware with groups of instances in different partitions. This strategy is typically used by large distributed and replicated workloads, such as Hadoop, Cassandra, and Kafka.
        

### **Placement group strategies:**

**Cluster placement groups:**

A cluster placement group is a logical grouping of instances within a single Availability Zone. A cluster placement group can span peered virtual private networks (VPCs) in the same Region. Instances in the same cluster placement group enjoy a higher per-flow throughput limit for TCP/IP traffic and are placed in the same high-bisection bandwidth segment of the network.

The following image shows instances that are placed into a cluster placement group.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690467292421/1ab0c5dd-1289-4a34-b6c5-41d135835dc3.jpeg align="center")

**Use case:**

* Big Data job that needs to complete fast
    
* The application that needs extremely low latency and high network throughput
    

### **Partition placement groups:**

Partition placement groups help reduce the likelihood of correlated hardware failures for your application. When using partition placement groups, Amazon EC2 divides each group into logical segments called partitions. Amazon EC2 ensures that each partition within a placement group has its own set of racks. Each rack has its own network and power source. No two partitions within a placement group share the same racks, allowing you to isolate the impact of a hardware failure within your application.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690467668315/00d7df94-1327-444a-9c97-c1ae8ead89a0.jpeg align="center")

**Use case:** HDFS, HBase, Cassandra, Kafka

### **Spread placement groups:**

A spread placement group is a group of instances that are each placed on distinct hardware.

Spread placement groups are recommended for applications that have a small number of critical instances that should be kept separate from each other. Launching instances in a spread-level placement group reduces the risk of simultaneous failures that might occur when instances share the same equipment. Spread-level placement groups provide access to distinct hardware and are therefore suitable for mixing instance types or launching instances over time.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690467936616/93de5205-7118-4afc-af9f-c832997c755a.jpeg align="center")

**Use case:**

* An application that needs to maximize high availability
    
* Critical Applications where each instance must be isolated from failure from each other
    

Thank you, Happy Learning!