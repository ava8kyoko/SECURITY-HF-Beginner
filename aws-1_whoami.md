#  01 - AWS whoami (5)

## Challenge
In AWS, a user needs to generate an access key and a secret key to interact with the AWS API. 
Can you find out to whom this set of credentials belongs to?
- Access key: AKIATAAH6Q3WM3U5ORWT
- Secret key: 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
- Note: The us-east-1 AWS region is to be used for all challenges in this category.

## Steps
1. `sudo apt install awscli` (Installation of aws client)
2. `aws configure` (???)
```
AWS Access Key ID [None]: AKIATAAH6Q3WM3U5ORWT                  
AWS Secret Access Key [None]: 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
Default region name [None]: us-east-1
Default output format [None]: 

```
3. `aws iam help` (???)
4. `aws list-roles` (???)
```
An error occurred (AccessDenied) when calling the ListRoles operation: 
User: arn:aws:iam::206175110892:user/HF-0pI6PCRDMqLJkYkWHnZF94oobgYkmpiM 
is not authorized to perform: iam:ListRoles on resource: 
arn:aws:iam::206175110892:role/

```

## Flag
`HF-0pI6PCRDMqLJkYkWHnZF94oobgYkmpiM`
