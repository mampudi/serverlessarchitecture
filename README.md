# Serverless Architecture

Define: A serverless Architecture trades control and customerzation for increased development speed and reduced maintencance 
        The cloud provider runs the server and dynamically manages the allocation of machine resources

# No serverless
1. We need to own our own hardware, racks, coolking, access 
2. We own the OS layer meaning we are responsible for keeping our pached and secure
3. We are owning the data layer. log data etc
4. We are owning the application layer. the runtime etc

# Maximum control to minimum maintencance
1. IaaS - no longer relying on on prem hardware. azure, aws, google etc (still responsible for paching OS,managing data and application layer)
2. PaaS - no longer managing hardware and OS. (Still have to manage application and data layer)
3. Functions as a service - Hardware, OS is managed for us in additon we have a potion of data and application managed for us
4. SaaS - The platform itself manages the hardware, OS, Data and application layer (This is not for running out custom code)

# Architecture - 4 Pillars
1. Compute - Loigc apps, functionspass, lamba
2. Storage - storage accounts, S Bukets for static assests
3. Persistance - Sql, no sql, dynamo db etc
4. Eventing - (API Management and Azure Event Grid) (API Gateway and Kinesis Stream) - SQS

# Serverless Manifesto                                        
1. Speed of innovation over depth of customization
2. Deffered risk over extensive ownership
3. Cost for actual use over cost for predicted use
4. Scalability by default over scalability by design
5. Managed service over customer infrastructure

# Benefits                                                                Challenges
1. Reduction in long term maintenance                                   1. New architectural approach and new skills required
2. Increased speed of innovation                                        2. Decreased flexibility and control
3. Reduction is required core competencies (increased focus)            3. Limited in complience approach if not supported on platform
4. Risk and complience mitication                                       4. Requires a platform selection (potential for vendor lock-in)
5. Cost tied to usage
6. Handles scaling

# Solution Categories
1. Public Cloud - implemented on a public cloud provider - AWS compute with Lamda - Azure with functions and logic apps - Google Cloud platform - GCP
2. Cross platform - Solution that works on multiple platforms
3. Open Source - Implemented on a private or hybrid cloud

# Implementing
1. Identify complience needs (HIPPA etc)
2. Review core competencies for cloud
3. Identify 1 or 2 platforms
4. Select a pilot team
5. A pilot application
6. Education and implementation
7. Build a knowledge base
8. Business a server comunity of practice

# Niche Provider
1. Iron.io
2. Cloud Flare Workers
3. OpenFaaS 


# Looking into the serverless framework for 
1. simple and easy deployments
2. Easy to reproduce architecture
3. Local execution for deployment and debugging

# AWS Free Tier - 12 months for free
1. Amazon EC2
2. Lamda
3. Dynamo DB - No Sql
4. RDS - Relational Database Service
5. Simple Email Service
6. Simple Storage Service (S3)

# AWS Free Tier Examples
1. EC2 - 750 Hours
2. 1 Million Lamda function a month
3. 25 GB - dynamo db
4. 20 GB - RDS
5. S3 - 5 GB of files

# Services to use
1. Lambda
2. IAM 
3. Simple Email Service
4. Systems Manager Service - parameter store to save api keys
5. API Gateway
6. Dynamo DB Service

# IAM - Identity and Access Management
1. 

# AWS Lamda
1. Cloud watch logs
2. Cloud watch alrms to trigger and alert 

