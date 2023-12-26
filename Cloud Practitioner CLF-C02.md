# Cloud Practitioner CLF-C02

Reviewed: No

[https://d1.awsstatic.com/whitepapers/aws-overview.pdf](https://d1.awsstatic.com/whitepapers/aws-overview.pdf)

### Amazon EC2 ( elastic compute cloud ):

The service you use to access the virtual servers of aws is knows as EC2 ( highly flexible, quick )  

- vertical scaling
- You can control the networking aspect of EC2

### EC2 Instances Types

**General purpose instances** provide a balance of compute, memory, and networking resources.

- application servers
- gaming servers
- backend servers for enterprise applications
- small and medium databases

**Compute optimized instances** (high performance) are ideal for compute-bound applications that benefit from high-performance processors. Like general purpose instances, you can use compute optimized instances for workloads such as web, application, and gaming servers. ( high performance processor)

**Memory optimized instances** are designed to deliver fast performance for workloads that process large datasets in memory and enable you to run workloads with high memory needs and receive great performance. (high performance database).

**Accelerated computing instances** use hardware accelerators, or co processors, to perform some functions more efficiently than is possible in software running on CPUs. Examples of 
these functions include floating-point number calculations, graphics processing, and data pattern matching.

**Storage optimized instances** are designed for workloads that require high, sequential read and write access to large datasets on local storage. Examples of workloads suitable for storage 
optimized instances include distributed file systems, data warehousing applications, and high-frequency online transaction processing (OLTP) systems.

### EC2 Pricing

**On-Demand Instances** are ideal for short-term, irregular workloads that cannot be interrupted. No upfront costs or minimum contracts apply. The instances run continuously until you stop them, and you pay for only the compute time you use. On-Demand Instances include developing and testing applications and running applications that have unpredictable usage patterns.(not for more than a year)

**Standard Reserved Instances**: This option is a good fit if you know the EC2 instance type and size you need for your steady-state applications and in which AWS Region you plan to run them. Reserved Instances require you to state the **Instance type and size, Platform description (operating system), Tenancy.**

**Convertible Reserved Instances**: If you need to run your EC2 instances in different Availability Zones or different instance types, then Convertible Reserved Instances might be right for you. Note: You trade in a deeper discount when you require flexibility to run your EC2 instances. At the end of a Reserved Instance term, you can continue using the Amazon EC2 instance without interruption. However, you are charged On-Demand rates until you do one of the following:

- Terminate the instance.
- Purchase a new Reserved Instance that matches the instance attributes (instance family and size, Region, platform, and tenancy).

**EC2 Instance Savings Plans** reduce your EC2 instance costs when you make an hourly spend commitment to an instance family and Region for a 1-year or 3-year term. This term commitment results in savings of up to 72 percent compared to On-Demand rates. Any usage up to the commitment is charged at the discounted Savings Plans rate (for example, $10 per hour). Any usage beyond the commitment is charged at regular On-Demand rates. The EC2 Instance Savings Plans are a good option if you need flexibility in your Amazon EC2 usage over the duration of the commitment term. You have the benefit of saving costs on running any EC2 instance within an EC2 instance family in a chosen Region (for example, M5 usage in N. Virginia) regardless of Availability Zone, instance size, OS, or tenancy. The savings with EC2 Instance Savings Plans are similar to the savings provided by Standard Reserved Instances.

**Spot Instances** are ideal for workloads with flexible start and end times, or that can withstand interruptions. Spot Instances use unused Amazon EC2 computing capacity and offer you cost savings at up to 90% off of On-Demand prices.

**Dedicated Hosts** are physical servers with Amazon EC2 instance capacity that is fully dedicated to your use. You can use your existing per-socket, per-core, or per-VM software licenses to help maintain license compliance. You can purchase On-Demand Dedicated Hosts and Dedicated Hosts Reservations. Of all the Amazon EC2 options that were covered, Dedicated Hosts are the most expensive.

## Scalability

It involves beginning with only the resources you need and designing your architecture to automatically respond to changing demand by scaling out or in. As a result, you pay for only the resources you use. You don’t have to worry about a lack of computing capacity to meet your customers’ needs. Amazon EC2 Auto Scaling enables you to automatically add or remove Amazon EC2 instances in response to changing application demand

Amazon EC2 Auto Scaling, you can use two approaches: dynamic scaling and predictive scaling.

- *Dynamic scaling* responds to changing demand.
- *Predictive scaling* automatically schedules the right number of Amazon EC2 instances based on predicted demand.

![Untitled](Cloud%20Practitioner%20CLF-C02%20cfc50fae4bda44eb8532977274860d1f/Untitled.png)

## **Elastic Load Balancing**

It is the AWS service that automatically distributes incoming application traffic across multiple resources, such as Amazon EC2 instances. Low-demand period, High-demand period.

**Monolithic application:** include databases, servers, the user interface, business logic, and so on. In this approach to application architecture, if a single component fails, other components fail, and possibly the entire application fails.

**microservices:** application components are loosely coupled. In this case, if a single component fails, the other components continue to work because they are communicating with each other. The 
loose coupling prevents the entire application from failing.

**Amazon Simple Notification Service (Amazon SNS)** is a publish/subscribe service. Using Amazon SNS topics, a publisher publishes messages to subscribers. This is similar to the coffee shop; the cashier provides coffee orders to the barista who makes the drinks. In Amazon SNS, subscribers can be web servers, email addresses, AWS Lambda functions, or several other options.

**Amazon Simple Queue Service (Amazon SQS)** is a message queuing service. Using it you can send, store, and receive messages between software components, without losing messages or requiring other services to be available. In Amazon SQS, an application sends messages into a queue. A user or service retrieves a message from the queue, processes it, and then deletes it from the queue. This decoupled approach enables the separate components to work more efficiently and independently.

## **Server less computing**

The term “server less” means that your code runs on servers, but you do not need to provision or manage these servers. With server less computing, you can focus more on innovating new products and features instead of maintaining servers. Another benefit of server less computing is the flexibility to scale server less applications automatically. Server less computing can adjust the applications' capacity by modifying the units of consumptions, such as throughput and memory.

## **AWS Lambda**

**[AWS Lambda](https://aws.amazon.com/lambda)** is a service that lets you run code without needing to provision or manage servers. While using AWS Lambda, you pay only for the compute time that you consume. Charges apply only when your code is running. You can also run code for virtually any type of application or backend service, all with zero administration.

## **Containers**

**Containers** provide you with a standard way to package your application's code and dependencies into a single object. You can also use containers for processes and workflows in which there are essential requirements for security, reliability, and scalability.

## **Amazon Elastic Container Service (Amazon ECS)**

**[Amazon Elastic Container Service (Amazon ECS)](https://aws.amazon.com/ecs/)** is a highly scalable, high-performance container management system that enables you to run and scale containerized applications on AWS.

Amazon ECS supports Docker containers. Docker is a software platform that enables you to build, test, and deploy applications quickly. AWS supports the use of open-source Docker Community Edition and subscription-based Docker Enterprise Edition. With Amazon ECS, you can use API calls to launch and stop Docker-enabled applications.

## **Amazon Elastic Kubernetes Service (Amazon EKS)**

**[Amazon Elastic Kubernetes Service (Amazon EKS)](https://aws.amazon.com/eks/)** is a fully managed service that you can use to run Kubernetes on AWS. Kubernetes is open-source software that enables you to deploy and manage containerized applications at scale. A large community of volunteers maintains Kubernetes, and AWS actively works together with the Kubernetes community. As new features and functionalities release for Kubernetes applications, you can easily apply these updates to your applications managed by Amazon EKS.

## **AWS Fargate**

**[AWS Fargate](https://aws.amazon.com/fargate/)** is a server less compute engine for containers. It works with both Amazon ECS and Amazon EKS. When using AWS Fargate, you do not need to provision or manage servers. AWS Fargate manages your server infrastructure for you. You can focus more on innovating and developing your applications, and you pay only for the resources that are required to run your containers.

### Selecting a region

- Compliance with data governance and legal requirements.
- Proximity to your customers.
- Available services within a Region.
- Pricing.

**AWS Management Console** is a web-based interface for accessing and managing AWS services. You can quickly access recently used services and search for other services by name, keyword, or 
acronym. The console includes wizards and automated workflows that can simplify the process of completing tasks. You can also use the AWS Console mobile application to perform tasks such as monitoring resources, viewing alarms, and accessing billing information. Multiple identities can stay logged into the AWS Console mobile app at the same time.

**AWS Command Line Interface (AWS CLI)**. AWS CLI enables you to control multiple AWS services directly from the command line within one tool. AWS CLI is available for users on Windows, macOS, and Linux.

**Software development kits (SDKs)**. SDKs make it easier for you to use AWS services through an API designed for your programming language or platform. SDKs enable you to use AWS services with your existing applications or create entirely new applications that will run on AWS. Languages include C++, Java, .NET, and more.

**AWS Elastic Beanstalk**, you provide code and configuration settings, and Elastic Beanstalk deploys the resources necessary to perform the following tasks:

- Adjust capacity
- Load balancing
- Automatic scaling
- Application health monitoring

**AWS CloudFormation**, you can treat your infrastructure as code. This means that you can build an environment by writing lines of code instead of using the AWS Management Console to individually provision resources. AWS CloudFormation provisions your resources in a safe, repeatable manner, enabling you to frequently build your infrastructure and applications without having to perform manual actions. It determines the right operations to perform when managing your stack and rolls back changes automatically if it detects errors.

**Amazon CloudFront** is a content delivery service. It uses a network of edge locations to cache content and deliver content to customers all over the world. When content is cached, it is stored locally as a copy. This content might be video files, photos, webpages, and so on.

## Networking

- A **subnet** is a section of a VPC that can contain resources such as Amazon EC2 instances.
- To allow public traffic from the internet to access your VPC, you attach an **internet gateway** to the VPC.
- A virtual private gateway enables you to establish a virtual private network (VPN) connection between your VPC and a private network
- Security groups are stateful. This means that they use previous traffic patterns and flows when evaluating new requests for an instance. Security groups deny all inbound traffic, but you can add custom rules to fit your operational and security needs.
- An edge location is a site that Amazon CloudFront uses to store cached copies of your content for faster delivery to customers.
- A security group is a virtual firewall that controls inbound and outbound traffic for an Amazon EC2 instance.
- Amazon Route 53 is a DNS web service. It gives developers and businesses a reliable way to route end users to internet applications that host in AWS. Another feature of Route 53 is the ability to manage the DNS records for domain names. You can transfer DNS records for existing domain names managed by other domain registrars. You can also register new domain names directly in Route 53.
- Amazon Virtual Private Cloud (Amazon VPC) is a service that enables you to provision an isolated section of the AWS Cloud. In this isolated section, you can launch resources in a
virtual network that you define.
- AWS Direct Connect is a service that enables you to establish a dedicated private connection between your data center and VPC.
- Amazon CloudFront is a content delivery service. It uses a network of edge locations to cache content and deliver content to customers all over the world.

# Storage & Databases

Amazon EC2 instances are virtual servers. If you start an instance from a stopped state, the instance might start on another host, where the previously used instance store volume does not exist. Therefore, AWS recommends instance stores for use cases that involve temporary data that you do not need in the long term.

An [**i](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html)nstance store** provides temporary block-level storage for an Amazon EC2 instance. An instance store is disk storage that is physically attached to the host computer for an EC2 instance, and therefore has the same lifespan as the instance.

**Amazon Elastic Block Store** is a service that provides block-level storage volumes that you can use with Amazon EC2 instances. If you stop or terminate an Amazon EC2 instance, all the data on the attached EBS volume remains available.

An **[EBS snapshot](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSSnapshots.html)** is an incremental backup. This means that the first backup taken of a volume copies all the data. For subsequent backups, only the blocks of data that have changed since the most recent snapshot are saved.

**Amazon Simple Storage Service (Amazon S3)**

**[Amazon Simple Storage Service (Amazon S3)](https://aws.amazon.com/s3/)** is a service that provides object-level storage. Amazon S3 stores data as objects in buckets. You can upload any type of file to Amazon S3, such as images, videos, text files, and so on. For example, you might use Amazon S3 to store backup files, media files for a website, or archived documents. Amazon S3 offers unlimited storage space. The maximum file size for an object in Amazon S3 is 5 TB. When you upload a file to Amazon S3, you can set permissions to control visibility and access to it. You can also use the Amazon S3 versioning feature to track changes to your objects over time.

- S3 Standard+
    - Designed for frequently accessed data
    - Stores data in a minimum of three Availability Zones
    - Costly than others.
- S3 Standard-Infrequent Access (S3 Standard-IA)+
    - Ideal for infrequently accessed data
    - Similar to Amazon S3 Standard but has a lower storage price and higher retrieval price
    - Lower storage price but higher retrieval price.
- S3 One Zone-Infrequent Access (S3 One Zone-IA)+
    - Stores data in a single Availability Zone
    - Has a lower storage price than Amazon S3 Standard-IA
- S3 Intelligent-Tiering+
    - Ideal for data with unknown or changing access patterns
    - Requires a small monthly monitoring and automation fee per object
- S3 Glacier Instant Retrieval+
    - Can retrieve objects within a few milliseconds
    - Works well for archived data that requires immediate access
- S3 Glacier Flexible Retrieval+
    - Low-cost storage designed for data archiving
    - Able to retrieve objects within a few minutes to hours
- S3 Glacier Deep Archive+
    - Lowest-cost object storage class ideal for archiving
    - Able to retrieve objects within 12 hours
    - lowest cost
- S3 Outposts+
    - Creates S3 buckets on Amazon S3 Outposts
    - Makes it easier to retrieve, store, and access data on AWS Outposts
    - used when data is required to reside close to on-premise .
- **Amazon EFS** is a regional service. It stores data in and across **multiple** Availability Zones. The duplicate storage enables you to access data concurrently from all the Availability Zones in the Region where a file system is located. Additionally, on-premises servers can access Amazon EFS using AWS Direct Connect.

**Amazon RDS** is available on six database engines, which optimize for memory, performance, or input/output (I/O). Supported database engines include:

- Amazon Aurora ( 5*MySQL & 3*PostgreSQL faster)
- PostgreSQL
- MySQL
- MariaDB
- Oracle Database
- Microsoft SQL Server

**Amazon Aurora** helps to reduce your database costs by reducing unnecessary input/output (I/O) operations, while ensuring that your database resources remain reliable and available.
MySQL, postgreSQL.

Consider Amazon Aurora if your workloads require high availability. It replicates six copies of your data across three Availability Zones and continuously backs up your data to Amazon S3. 

**Amazon DynamoDB** is a key-value database service. It delivers single-digit millisecond performance at any scale.

1. Server less: DynamoDB is server less, which means that you do not have to provision, patch, or manage servers. You also do not have to install, maintain, or operate software.
2. Automatic scaling :As the size of your database shrinks or grows, DynamoDB automatically scales to adjust for changes in capacity while maintaining consistent performance. This makes it a suitable choice for use cases that require high performance while scaling.

**Amazon RedShift** is a data warehousing service that you can use for big data analytics. It offers the ability to collect data from many sources and helps you to understand relationships and trends across your data.

**Amazon Database Mitigation Service** With AWS DMS, you move data between a source database and a target database. [The source and target databases](https://aws.amazon.com/dms/resources) can be of the same type or different types. During the migration, your source database remains operational, reducing downtime for any 
applications that rely on the database. Uses: Development and test database, Continuous replication, Database consolidation.

**[Amazon DocumentDB](https://aws.amazon.com/documentdb)** is a document database service that supports MongoDB workloads. (MongoDB is a document database program.)

**[Amazon Neptune](https://aws.amazon.com/neptune)** is a graph database service. You can use Amazon Neptune to build and run applications that work with highly connected datasets, such as recommendation engines, fraud detection, and knowledge graphs.

**[Amazon Quantum Ledger Database (Amazon QLDB)](https://aws.amazon.com/qldb)** is a ledger database service. You can use Amazon QLDB to review a complete history of all the changes that have been made to your application data.

**[Amazon Managed Blockchain](https://aws.amazon.com/managed-blockchain)** is a service that you can use to create and manage blockchain networks with open-source frameworks. Blockchain is a distributed ledger system that lets multiple parties run transactions and share data without a central authority.

**[Amazon ElastiCache](https://aws.amazon.com/elasticache)** is a service that adds caching layers on top of your databases to help improve the read times of common requests. It supports two types of data stores: Redis and Memcached.

**[Amazon DynamoDB Accelerator (DAX)](https://aws.amazon.com/dynamodb/dax/)** is an in-memory cache for DynamoDB. It helps improve response times from single-digit milliseconds to microseconds.

# Security

customer - security in cloud
AWS - security of cloud 

### IAM - Identity & Access Management

IAM root
IAM user
IAM Policy
IAM Group
IAM Roles
Multi-factor authentication ( MFA )

You can use **[AWS Organizations](https://aws.amazon.com/organizations)** to consolidate and manage multiple AWS accounts within a central location. When you create an organization, AWS Organizations automatically creates a **root**, which is the parent container for all the accounts in your organization. In AWS Organizations, you can centrally control permissions for the accounts in your organization by using Service Control Policies. SCPs enable you to place restrictions on the AWS services, resources, and individual API actions that users and roles in each account can access.

**SCPs -** organization root, an individual member account, or an OU. An SCP affects all IAM users, groups, and roles within an account, including the AWS account root user.

**IAM policies -** IAM users, groups, or roles. Can’t apply on root user

**AWS Artifact** is a service that provides on-demand access to AWS security and compliance reports and select online agreements. AWS Artifact consists of two main sections: AWS Artifact Agreements (review, accept, and manage agreements for individual and all ) and AWS Artifact Reports ( provide compliance reports from third-party auditors ).

**AWS Shield** is a service that protects applications against DDoS attacks. AWS Shield provides two levels of protection: Standard ( no cost, analyse traffic in real time and automatically mitigates it ) and Advanced ( paid , provides detailed attack diagnostics and the ability to detect and mitigate sophisticated DDoS attacks. and also integrates with other services such as Amazon CloudFront, Amazon Route 53, and Elastic Load Balancing. Additionally, you can integrate AWS Shield with AWS WAF by writing custom rules to mitigate complex DDoS attacks ).

**AWS Key Management Service (AWS KMS)** enables you to perform encryption operations through the use of **cryptographic keys**. A cryptographic key is a random string of digits used for locking 
(encrypting) and unlocking (decrypting) data. You can use AWS KMS to create, manage, and use cryptographic keys. You can also control the use of keys across a wide range of services and in your applications.

**Amazon Inspector** helps to improve the security and compliance of applications by running automated security assessments. It checks applications for security vulnerabilities and deviations from security best practices, such as open access to Amazon EC2 instances and installations of vulnerable software versions.

**Amazon GuardDuty** is a service that provides intelligent threat detection for your AWS 
infrastructure and resources. It identifies threats by continuously monitoring the network activity and account behavior within your AWS environment.

# Monitoring and Analytics

**Amazon CloudWatch** is a web service that enables you to monitor and manage various metrics
and configure alarm actions based on data from those metrics. CloudWatch uses **metrics** [](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/working_with_metrics.html)to represent the data points for your resources. AWS services send metrics to CloudWatch. CloudWatch then uses these metrics to create graphs automatically that show how performance has changed over time. you can create **[alarms](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html)** that automatically perform actions if the value of your metric has gone above or below a predefined threshold.

**AWS CloudTrail** records API calls for your account. The recorded information includes the identity of the API caller, the time of the API call, the source IP address of the API caller, and more. You can think of CloudTrail as a “trail” of breadcrumbs (or a log of actions) that someone has left behind them. Updates after 15 minutes. **CloudTrail Insights** automatically detect unusual API activities in your AWS account.

**AWS Trusted Advisor** is a web service that inspects your AWS environment and provides real-time recommendations in accordance with AWS best practices. **cost optimization, performance, security, fault tolerance, and service limits.  
Green check -** no problem.
**Orange Triangle -** indicated number of recommended investigations.
**Red circle -** number of recommended actions. ****

# Pricing and Support

[AWS Support Plan Comparison | Developer, Business, Enterprise, Enterprise On-Ramp | AWS Support](https://aws.amazon.com/premiumsupport/plans/)

**AWS Free Tier** enables you to begin using certain services without having to worry about incurring costs for the specified period.

- Always Free - AWS Lambda allows 1 million free requests and up to 3.2 million seconds of compute time per month. Amazon DynamoDB allows 25 GB of free storage per month.
- 12 Months Free - specific amounts of Amazon S3 Standard Storage, thresholds for monthly hours of Amazon EC2 compute time, and amounts of Amazon CloudFront data transfer out.
- Trials - Amazon Inspector offers a 90-day free trial. Amazon Lightsail (a service that enables you to run virtual private servers) offers 750 free hours of usage over a 30-day period.

**Amazon Billing Dashboard**

- Compare your current month-to-date balance with the previous month, and get a forecast of the next month based on current usage.
- View month-to-date spend by service.
- View Free Tier usage by service.
- Access Cost Explorer and create budgets.
- Purchase and manage Savings Plans.
- Publish AWS Cost and Usage Reports

**Consolidated billing** feature of AWS Organizations enables you to receive a single bill for all AWS accounts in your organization. By consolidating, you can easily track the combined costs of all the linked accounts in your organization. The default maximum number of accounts allowed for an organization is 4, but you can contact AWS Support to increase your quota, if needed.

**AWS Cost Explorer** is a tool that lets you visualize, understand, and manage your AWS costs and usage over time. It includes a default report of the costs and usage for your top five cost-accruing AWS services. You can apply custom filters and groups to analyze your data. For example, you can view resource usage at the hourly level.

**Basic Support** is free for all AWS customers. It includes access to whitepapers, documentation, and support communities. With Basic Support, you can also contact AWS for billing questions and 
service limit increases.

**The Developer, Business, Enterprise On-Ramp, and Enterprise Support -** includes basic support, unlimited support cases, pay-by-month, no long term contract

**Developer Support** plan have access to features such as:

- Best practice guidance
- Client-side diagnostic tools
- Building-block architecture support, which consists of guidance for how to use AWS offerings, features, and services together

**Business Support** plan have access to additional features, including:

- Use-case guidance to identify AWS offerings, features, and services that can best support your specific needs
- All AWS Trusted Advisor checks
- Limited support for third-party software, such as common operating systems and application stack components

**AWS Enterprise On-Ramp Support plan** includes basic, developer, business support plans and :

- A pool of Technical Account Managers to provide proactive guidance and coordinate access to programs and AWS experts
- A Cost Optimization workshop (one per year)
- A Concierge support team for billing and account assistance
- Tools to monitor costs and performance through Trusted Advisor and Health API/Dashboard
- Consultative review and architecture guidance (one per year)
- Infrastructure Event Management support (one per year)
- Support automation workflows
- 30 minutes or less response time for business-critical issues

The **TAM** is your primary point of contact at AWS. If your company subscribes to Enterprise Support or Enterprise On-Ramp, your TAM educates, empowers, and evolves your cloud journey across the full range of AWS services. TAMs provide expert engineering guidance, help you design solutions that efficiently integrate AWS services, assist with cost-effective and resilient architectures, and provide direct access to AWS programs and a broad community of experts.

**Only the Business, Enterprise On-Ramp, and Enterprise Support plans include all AWS Trusted Advisor checks. Of these three Support plans, the Business Support plan has a lower cost.**

**AWS Marketplace** is a digital catalog that includes thousands of software listings from 
independent software vendors. You can use AWS Marketplace to find, test, and buy software that runs on AWS. Infrastructure Software, DevOps, Data Products, Professional Services, Business Applications, Machine Learning, Industries, and Internet of Things (IoT).

# Migration & innovation

### **AWS Cloud Adoption Framework (AWS CAF)**

It organizes guidance into six areas of focus, called **Perspectives**. Each Perspective addresses distinct responsibilities. The planning process helps the right people across the organization prepare for the changes ahead.
**Business**, **People**, and **Governance** Perspectives focus on business capabilities.
**Platform**, **Security**, and **Operations** Perspectives focus on technical capabilities.

****Business Perspective**** ensures that IT aligns with business needs and that IT investments link to key business results.

- Business managers
- Finance managers
- Budget owners
- Strategy stakeholders

**People Perspective** supports development of an organization-wide change management strategy for successful cloud adoption.

- Human resources
- Staffing
- People managers

**Governance Perspective** focuses on the skills and processes to align IT strategy with business strategy. This ensures that you maximize the business value and minimize risks.

- Chief Information Officer (CIO)
- Program managers
- Enterprise architects
- Business analysts
- Portfolio managers

**Platform Perspective** includes principles and patterns for implementing new solutions on the cloud, and migrating on-premises workloads to the cloud.

- Chief Technology Officer (CTO)
- IT managers
- Solutions architects

**Security Perspective** ensures that the organization meets security objectives for visibility, auditability, control, and agility.

- Chief Information Security Officer (CISO)
- IT security managers
- IT security analysts

**Operations Perspective** helps you to enable, run, use, operate, and recover IT workloads to the level agreed upon with your business stakeholders.

- IT operations managers
- IT support managers

### ****6 strategies for migration****

- Rehosting - lift-and-shift, without changes, most applications are rehosted.
- Replatforming - lift, tinker, and shift, few cloud optimizations, no change in the core architecture of the application.
- Refactoring/re-architecting - **re-architecting,** to add features, scale, or performance
- Repurchasing - moving from a traditional license to a software-as-a-service model.
- Retaining - keeping applications that are critical for the business in the source environment
- Retiring - process of removing applications that are no longer needed.

### AWS Snow Family

It is a collection of physical devices that help to physically transport up to exabytes of data into and out of AWS. . It includes AWS security, monitoring, storage management, and computing capabilities.

- **AWS Snowcone -** It is a small, rugged, and secure edge computing and data transfer device. It features **2 CPUs, 4 GB of memory, and up to 14 TB of usable storage.**
- **AWS Snowball -**
    - **Snowball Edge Storage Optimized** devices are
    well suited for large-scale data migrations and recurring transfer
    workflows, in addition to local computing with higher capacity needs.
        - Storage: 80 TB of hard disk drive (HDD) capacity for block volumes and Amazon S3 compatible object storage, and 1 TB of SATA solid state drive (SSD) for block volumes.
        - Compute: 40 vCPUs, and 80 GiB of memory to support Amazon EC2 sbe1 instances (equivalent to C5).
    - **Snowball Edge Compute Optimized** provides powerful computing resources for use cases such as machine learning,
    full motion video analysis, analytics, and local computing stacks.
        - Storage: 80-TB usable HDD capacity for Amazon S3 compatible object storage or
        Amazon EBS compatible block volumes and 28 TB of usable NVMe SSD
        capacity for Amazon EBS compatible block volumes.
        - Compute: 104
        vCPUs, 416 GiB of memory, and an optional NVIDIA Tesla V100 GPU. Devices run Amazon EC2 sbe-c and sbe-g instances, which are equivalent to C5,
        M5a, G3, and P3 instances.
- **AWS Snowmobile -** It is an exabyte-scale data transfer service used to move large amounts of data to AWS. You can transfer up to 100 petabytes of data per Snowmobile, a 45-foot long ruggedized shipping container, pulled by a semi trailer truck.

### Innovation

**serverless** refers to applications that don’t require you to provision, maintain, or administer servers.

- **Amazon Transcribe -** Convert speech to text.
- **Amazon Comprehend -** Discover patterns in text.
- **Amazon Fraud Detector -** Identify potentially fraudulent online activities.
- **Amazon Lex -** Build voice and text chatbots.
- ***Amazon Textract -*** extracts text and data from scanned document.
- ***Amazon DocumentDB** -* A document database service that supports MongoDB workloads.
- **Amazon SageMaker -**  build, train, and deploy ML models quickly.
- **Amazon Polly** is a machine learning service that converts text to speech. This service provides the ability to read text out loud.

## THE CLOUD JOURNEY

**The Well-Architected Framework** is based on six pillars:

- Operational excellence - run and monitor systems to deliver business value and to continually improve supporting processes and procedures.
- Security - protect information, systems, and assets while delivering business value through risk assessments and mitigation strategies.
- Reliability - testing recovery procedures, scaling horizontally to increase aggregate system availability, and automatically recovering from failure.
- Performance efficiency - use computing resources efficiently to meet system requirements and to maintain that efficiency as demand changes and technologies evolve.
- Cost optimization - run systems to deliver business value at the lowest price point. Cost optimization includes adopting a consumption model, analyzing and attributing expenditure, and using managed services to reduce the cost of ownership.
- Sustainability - continually improve sustainability impacts by reducing energy consumption and increasing efficiency across all components of a workload by maximizing the benefits from the provisioned resources and minimizing the total resources required. To facilitate good design for sustainability:
    - Understand your impact
    - Establish sustainability goals
    - Maximize utilization
    - Anticipate and adopt new, more efficient hardware and software offerings
    - Use managed services
    - Reduce the downstream impact of your cloud workloads

## Important:

- **multitenancy**: Sharing underlying hardware between virtual machines
- An **edge location** is a site that Amazon **CloudFront** uses to store cached copies of your content closer to your customers for faster delivery.
- AWS Outposts is a service that enables you to run infrastructure in a hybrid cloud approach.
- AWS Fargate is a serverless compute engine for containers.
- Amazon Simple Queue Service (Amazon SQS) is a service that enables you to send, store, and receive messages between software components through a queue.
- The AWS Management Console includes wizards and workflows that you can use to complete tasks in AWS services.
- The AWS Command Line Interface (AWS CLI) is used to automate actions for AWS services and applications through scripts.
- Software development kits (SDKs) enable you to develop AWS applications in supported programming languages
- **AWS Personal Health Dashboard**, a tool that provides alerts and remediation guidance when AWS is experiencing events that may affect you.
- **Amazon Macie** is a security service that uses machine learning to automatically discover, classify, and protect sensitive data, including personally identifiable information (PII)