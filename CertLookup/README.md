# CertLookup

This is a Cloudformation Macro that will lookup a CertificateArn for a particular DomainName within the HostedZone with the specified Domain.  It also sets a Condition CreateCertificate that can be referenced.  This will allow an AWS user to not surpass the ACM Certificate request quota when deploying their template multiple times or iteratively developing and testng out their changes.

# How to use

The first step is to install this macro into your AWS account in all regions where your CloudFormation templates will run.

```
aws cloudformation deploy --stack-name=<Macro Name> --region <Region> --template-file macro.template --capabilities CAPABILITY_NAMED_IAM 
```