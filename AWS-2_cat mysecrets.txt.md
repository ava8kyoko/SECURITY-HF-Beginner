#  AWS 02 - cat mysecrets.txt (6)

## Challenge
In AWS, Secrets Manager can act as a sort of password manager for your applications, 
and access to those secrets can be logged and restricted. Using the credentials given 
in the AWS whoami challenge, can you recover the flag stored it the following secrets 
manager's secret?
<br>
hf-aws-beginner-challenge2-secret

## Steps
1.`aws secretsmanager get-secret-value --secret-id hf-aws-beginner-challenge2-secret` (???)
```
{
    "ARN": "arn:aws:secretsmanager:us-east-1:206175110892:secret:hf-aws-beginner-challenge2-secret-bmddwG",
    "Name": "hf-aws-beginner-challenge2-secret",
    "VersionId": "044ddc94-5ed0-48dc-b772-1bee33939b3d",
    "SecretString": "HF-qomhnIEg7vBV1nkieT3CmtpKdagTTfzw",
    "VersionStages": [
        "AWSCURRENT"
    ],
    "CreatedDate": 1637026439.777
}
```

## Flag
`HF-qomhnIEg7vBV1nkieT3CmtpKdagTTfzw`
