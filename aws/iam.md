# IAM (Identity and Access Management)

IAM is an Identity and Access management tool. Basically, it gives users the chance to create new roles, groups and users that bind with some policies. Policies are important because as a default rule newly created users don't have permission to do something on the AWS services. If they don't have any granted permissions or are not added under some policy etc. I

In addition to that, every AWS service needs or is related to permissions. As a result, IAM needs to be reached by every user of it. For this purpose,  IAM made a **Global** service. It can be reached in any region and availability zones.

Now let's check details with sub-sections

### Users & Groups

* **Root** user is created by **default**. But it is advised to not used to this account except AWS account setup.
* Users can be grouped.
* Users can be joined into multiple groups and vice versa also they may not be into any group.
* **Groups** can't contain different groups. **Only includes users**.

### Permissions

* It is an extremely crucial feature of the IAM to give permission to the users and groups.
* Users or Groups can be assigned JSON documents called policies.
* Always follow the **least-privilege** rule. Don't give permissions to the users more than they need.&#x20;
* It is possible to give direct permissions to the users without adding to any groups etc.

### IAM Policies

* Policies can be thought definitions of permissions. Let's say we have two groups of users in our project. e.g. developers and interns. You created one policy for developers one for interns. Developers are able to retrieve, edit, and delete pieces of information on some services but interns policy only includes the only read-only permissions.
* Policies are JSON documents that composed of **Version**, **Id (optional)** and **Statement** fields.&#x20;
* Users can create custom policies that just include required permissions also they are able to use predefined policies too.
* Users can be attached to multiple policies.

You could see the example of the policy document

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "ListAndDescribe",
            "Effect": "Allow",
            "Action": [
                "dynamodb:List*",
                "dynamodb:DescribeReservedCapacity*",
                "dynamodb:DescribeLimits",
                "dynamodb:DescribeTimeToLive"
            ],
            "Resource": "*"
        },
        {
            "Sid": "SpecificTable",
            "Effect": "Allow",
            "Action": [
                "dynamodb:BatchGet*",
                "dynamodb:DescribeStream",
                "dynamodb:DescribeTable",
                "dynamodb:Get*",
                "dynamodb:Query",
                "dynamodb:Scan",
                "dynamodb:BatchWrite*",
                "dynamodb:CreateTable",
                "dynamodb:Delete*",
                "dynamodb:Update*",
                "dynamodb:PutItem"
            ],
            "Resource": "arn:aws:dynamodb:*:*:table/MyTable"
        }
    ]
}
```

### MFA (Multi-Factor Authentication)

* It provides more security for our accounts. Like root and IAM users.
* For success login => Password + Secure Device(e.g. phone, virtual MFA devices, Universal 2nd Factor Security Key (**U2F**)  ) you own required.
* Thanks to him we protect our accounts from stolen and hacking.

### Access to AWS accounts

There are 3 types of access to AWS accounts. These are via **AWS Management Console**, **Command Line Interface (CLI)** and **AWS Software Developer Kit (SDK)**

* Access Keys should <mark style="color:red;">**keep private**</mark> like passwords
* They can be created through AWS Console and users manage their own keys.
* Can be thought like Access Key ID => Username, Secret Access Key => Password
* **AWS CLI** is the command line tool that enables users to directly access the services.
* **AWS SDK** is the set of programming libraries that enable users to access resources and services programmatically. Supports many different programming languages.

### IAM Roles

* Some AWS services will need to perform actions on our behalf (e.g. one of our Lambda functions needs to access some data that is located on DynamoDB).
* In that situation, we will assign permissions to AWS services with **IAM Roles.**

### IAM Security Tools

* **IAM Credentials Report **<mark style="color:red;">**(account-level)**</mark>
* **IAM Access Advisor **<mark style="color:red;">**(user-level)**</mark>
