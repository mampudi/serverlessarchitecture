#### Table of Contents

- [Serverless Architecture](#ServerlessArchitecture)
- [Identity and Access Management](#IdentityandAccessManagement)

# Serverless Architecture Report

Define: A Serverless Architecture trades control and customization for increased development speed and reduced maintenance 
        The cloud provider runs the server and dynamically manages the allocation of machine resources

# No Serverless
1. We need to own our own hardware, racks, cooling, access 
2. We own the OS layer meaning we are responsible for keeping our patched and secure
3. We are owning the data layer. log data etc
4. We are owning the application layer. the runtime etc

# Maximum control to minimum maintenance
1. IaaS - no longer relying on on premises hardware. azure, aws, google etc (still responsible for patching OS,managing data and application layer)
2. PaaS - no longer managing hardware and OS. (Still have to manage application and data layer)
3. Functions as a service - Hardware, OS is managed for us in addition we have a potion of data and application managed for us
4. SaaS - The platform itself manages the hardware, OS, Data and application layer (This is not for running out custom code)

# Architecture - 4 Pillars
1. Compute - Logic apps, function apps, lambda
2. Storage - storage accounts, S Buckets for static assets
3. Persistence - Sql, no sql, dynamo db etc
4. Eventing - (API Management and Azure Event Grid) (API Gateway and Kinesis Stream) - SQS

# Serverless Manifesto                                        
1. Speed of innovation over depth of customization
2. Deferred risk over extensive ownership
3. Cost for actual use over cost for predicted use
4. Scalability by default over scalability by design
5. Managed service over customer infrastructure

# Benefits                                                                
1. Reduction in long term maintenance                                   
2. Increased speed of innovation                                        
3. Reduction is required core competencies (increased focus)            
4. Risk and compliance mitigation                                       
5. Cost tied to usage
6. Handles scaling

# Challenges
1. New architectural approach and new skills required
2. Decreased flexibility and control
3. Limited in compliance approach if not supported on platform
4. Requires a platform selection (potential for vendor lock-in)

# Solution Categories
1. Public Cloud - implemented on a public cloud provider - AWS compute with Lambda - Azure with functions and logic apps - Google Cloud platform - GCP
2. Cross platform - Solution that works on multiple platforms
3. Open Source - Implemented on a private or hybrid cloud

# Implementing
1. Identify compliance needs (HIPPA etc)
2. Review core competencies for cloud
3. Identify 1 or 2 platforms
4. Select a pilot team
5. A pilot application
6. Education and implementation
7. Build a knowledge base
8. Business a server community of practice

# Niche Provider
1. Iron.io
2. Cloud Flare Workers
3. OpenFaaS 


# Looking into the Serverless framework for 
1. simple and easy deployments
2. Easy to reproduce architecture
3. Local execution for deployment and debugging

# AWS Free Tier - 12 months for free
1. Amazon EC2
2. Lambda
3. Dynamo DB - No Sql
4. RDS - Relational Database Service
5. Simple Email Service
6. Simple Storage Service (S3)

# AWS Free Tier Examples
1. EC2 - 750 Hours
2. 1 Million Lambda function a month
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

# Identity and Access Management
1. Users - Individuals who log into AWS with an email and password combination
2. Groups - These are a collection of users which share permission policies
3. Roles - These are similar to users because they carry with them a set of permissions that determine what a role can do. They are different because they don't have access keys or logic credentials. They can be assumed by AWS users or services like lambda 

> Users can be put into an IAM group that offers them certain permissions. This way we can give only the resources needed by a developer to a developer and only the resources needed by a data scientist to a data scientist. Each of those groups would then have policies that are applicable for those different kinds of users and each of these group policies is determined by and IAM group policy JSON.  

> Users > Groups > Policies

> Roles are a more flexible concept that allows permissions to be granted to AWS users or AWS account resources etc.

## Sample IAM Policy

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": "service-prefix:action-name",
            "Resource": "*",
            "Condition": {
                "DateGreaterThan": {"aws:CurrentTime":"2020-04-01T00:00:00Z"},
                "DateLessThan": {"aws:CurrentTime":"2020-06-30T23:59:59Z"}
            }
        }
    ]
}
```
## IAM Best Practices

1. Strong Passwords and unique passwords
2. If you can, use 2 factor authentication with a ha rdware token or a mobile app like google authenticator 
3. Principle of least privilege - Limit access to permissions or services wherever possible
4. Be careful when using your root account

## AWS Policy Generator
>The AWS Policy Generator is a tool that enables you to create policies that control access to Amazon Web Services (AWS) products and resources.

<https://awspolicygen.s3.amazonaws.com/policygen.html>

# AWS Lambda
1. Cloud watch logs
2. Cloud watch alarms to trigger and alert 

