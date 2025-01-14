# 1	IAM (Identity and access management)
The IAM system in cloud providers give clients a way to give limited privliged access to employees and machines in their firm. This is because most clients of cloud providers aren't singular individuals but multi-individual corporations.

This privilaged access system is divided into the following categories:

| category    | description                                                                                                                   |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------- |
| users       | specify individual users who uniquely have certain privilages                                                                 |
| user groups | specify a range of users who present a number of people who have shared accesses and privilages                               |
| roles       | temporary access for services that is typically used for giving access to machines but could be used to give to users as well |
| policies    | JSON objects in which you can specify range of privilages ready to be given or taken from groups/users/roles                  |

Each privilage is implicitly assumed as **not allowed** and has to be explicitly assigned as allowed in order for users to enjoy the privilages
When giving privilages to users always adhere to the rule of explicit and specific privilage access on a **need to have** basis. in other words, make sure no user/group/service gets more privilage than it needs
# 2	VPC
Virtual Private Cloud is essentially a subnetting service inside AWS that specifies shared resources  between different racks/regions belonging to the organization not much unlike traditional subnetting in traditional networks but this is available in AWS scalable infrastructure.

within the CIDR block you specify the range if IPs reserved for your use and the subnet mask.

You can either have private subnets for communication inside the AWS infrastracture without being exposed to the outer extranet. This doesn't mean that outsiders can't access this module though, they can do so but only with the use of the NAT gateway which redirects outside traffic to this module if configured.

public subnets don't need this extra step though and are inherently accessable to outside traffic.

# 3	EC2
Elasic Compte Cloud is a scalability service in  AWS that gives clients who have instances in AWS the ability to wasily scale up an down down their application based on demand, while still having the pricing be on demand. Even the storage is elasic with EBS(Elastic Block Store). Also the IP subnets can be elastic as well.
# 4	DynamoDB

DynamoDB is yet another service present in AWS that clients can choose to use. It's a fully managed, NoSQL, serverless. It can handle high-performance applications at any scale with high availability and low latency.
- It is only present as an AWS service. So it cannot be used in an on-premises or hybrid cloud solutions
- it uses nosql in that it abandons the usual SQL and instead proprietry API based on JSON that sets key-value pairs
- it does not support relational DBMS through usage of foreign keys to join tables.
# 5	Lambda
It is yet again another service provided by AWS. It is a serverless function as a service (FaaS) that enable developers to turn code into product in seconds without worrying about setting up runtimes, clusters, server management, scaling, or anything else.
- Code written is packaged into a lambda function that directly interacts as the core execution unit.
- They are triggered by events.
- They are scalable. Which means the function is scaled appropriately in response to traffic.
- When the function completes Lamda terminates the resources so that it doesn't further affect payment more than it has to.
# 6	S3
Simple Storage Service is a storage solution by AWS that stores all kinds of data, images, text, video, etc, as objects in buckets. This data can range from bytes to Petabytes. This also integrates with the IAM very well which gives you the ability to assign privilaged access to the data.
- You can specify regions for the data to optimize for performance or regulatory requirements.
- it offers durabiltiy of data that is almost perfecly guarenteed, versioning and security.
- it is priced according to the amount of data stored inside.