# Aws interview questions
---
## EC2 (Elastic Compute Cloud)
1. What is EC2?
- EC2 is a scalable, flexible and high performance compute service provided by aws cloud which provides virtual servers in the cloud.

2. What is the difference between an AMI and a snapshot?
- AMI: A template for launching EC2 instances (includes OS and apps).
- Snapshot: A backup of EBS volumes attached to EC2 instances.

3. How does EC2 instance pricing work?
- On-Demand: Pay for what you use.
- Spot: Bid for unused capacity.
- Reserved: Discounted rates for long-term use.

4. What is Elastic IP in EC2?
- An Elastic IP is a static IPv4 address that can be associated with any instance in your account.

5. What are the different instance types in EC2?
- General Purpose: Balanced compute, memory, and networking (e.g., t2, t3).
- Compute Optimized: High-performance computing (e.g., c5, c6).
- Memory Optimized: For memory-intensive applications (e.g., r5, x1).
- Storage Optimized: For high disk throughput (e.g., i3, d2).
---
## EBS (Elastic Block Store)

1. What is EBS?
- EBS provides block storage that can be attached to EC2 instances for persistent data storage.

2. What is volumes?
- volumes are the block level storage provided by AWS.

3. How do you back up EBS volumes?
- By creating a snapshot, which is stored in S3.

4. What is the difference between EBS and instance store?
- EBS Volumes: EBS Volumes are often used to provide persistent storage that remains intact even after EC2 instance stops and starts.
- Instance Store: "Instance Store" refers to temporary storage that is physically attached to EC2 instances,

5. What happens to the data on an EBS volume when an EC2 instance is terminated?
- If "Delete on Termination" is enabled, the volume is deleted; otherwise, it persists.
---