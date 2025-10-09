# Identity Account Architecture

## Understanding the Challenge

If an organization uses multiple sets of AWS accounts, having separate
usernames and passwords for each AWS account for users is a challenge.

![My Image](images/image1.png)

## Identity Account Architecture

In Identity Account architecture, the IAM users are created and managed in
central AWS Account.
From this central AWS account, they can login to any other AWS accounts.

![My Image](images/image2.png)

### Reference Screenshot


![My Image](images/image3.png)


## The Practical Architecture

![My Image](images/image4.png)

## Advantages and Disadvantages

**Advantages:**
- Simple setup with no extra costs. Fast to configure.

**Disadvantages:**
- Hard to manage when number of roles and AWS accounts increases.
- AWS console access is required for Switch Role operations.

## Practical Workflow Steps

- Create a user in Account A (Identity Account)
- Create a Cross-Account IAM Role in the destination account with
  appropriate trust and policies.
- Allow User to switch to CrossAccountRole.

## Reference Screenshot - STS Assume Role Policy

![My Image](images/image5.png)

## Point to Note

You cannot switch to a role when you sign in as the AWS account root user.