# What is AWS CloudFormation?

AWS CloudFormation is a service that helps you model and set up your Amazon Web Services resources. 
You create a template that describes all the AWS resources that you want (like Amazon EC2 instances or Amazon S3 buckets), 
and AWS CloudFormation takes care of provisioning and configuring those resources for you.

This allows you to:
- Manage infrastructure as code
- Automate deployments
- Ensure consistency across environments
- Easily replicate environments for development, testing, and production

CloudFormation supports YAML and JSON formats for templates and integrates with other AWS services to provide a powerful infrastructure automation solution.


# CloudFormation Basic Lab

This project contains basic AWS CloudFormation templates to create an S3 bucket and an EC2 instance.

## Files

- `templates/s3-bucket.yaml`: CloudFormation template for an S3 bucket
- `templates/ec2-instance.yaml`: CloudFormation template for an EC2 instance
- `README.md`: Project description

## How to Use

1. Open AWS CloudFormation Console.
2. Upload the desired template file.
3. Deploy the stack.

Sample code to create EC2 Instance via Cloudformation :

AWSTemplateFormatVersion: '2010-09-09'
Description: Basic CloudFormation Template to create an EC2 instance

Resources:
  MyEC2Instance:
    Type: AWS::EC2::Instance
    Properties:
      InstanceType: t2.micro
      ImageId: ami-0c02fb55956c7d316  # Amazon Linux 2 AMI (example, region-specific)
      KeyName: my-key-pair  # Replace with your actual key pair name
      Tags:
        - Key: Name
          Value: BasicEC2Instance


Sample code to create S3 bucket via Cloudformation :

AWSTemplateFormatVersion: '2010-09-09'
Description: Basic CloudFormation Template to create an S3 bucket

Resources:
  MyS3Bucket:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: !Sub 'my-basic-lab-bucket-${AWS::AccountId}'
