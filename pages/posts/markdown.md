---
title: Creating Nested Stacks with AWS SAM Python Package
date: 2023/04/13
description: Nested stacks are a powerful feature in AWS CloudFormation.
tag: AWS
author: You
---
Nested stacks are a powerful feature in AWS CloudFormation that allow you to break down a large stack into smaller, more manageable components. With nested stacks, you can define resources in a separate CloudFormation template, and then include that template as a resource in your parent template.

In this blog post, we'll show you how to create a nested stack using the AWS Serverless Application Model (SAM) with the Python package.

To get started, create a new folder for your nested stack, and navigate into it. Inside the nested stack folder, create a new file named **"template.yaml"** (or "template.yml"), which will define your nested stack resources. In the **"template.yaml"** file, define your resources using the SAM syntax, just like you would for a regular SAM template.

Next, use the **AWS::CloudFormation::Stack** resource to define a nested stack resource in your **"template.yaml"** file. The Properties section of this resource should include a TemplateURL property that points to the URL of your parent stack's template file. For example:

```
Resources:
  MyNestedStack:
    Type: 'AWS::CloudFormation::Stack'
    Properties:
      TemplateURL: https://s3.amazonaws.com/my-bucket/my-parent-stack.yaml
      Parameters:
        MyParam: !Ref MyParam
```
This code block defines a nested stack resource named **"MyNestedStack"** that includes a CloudFormation template located at **https://s3.amazonaws.com/my-bucket/my-parent-stack.yaml**. The Parameters section allows you to pass parameters from the parent stack to the nested stack.

Save the **"template.yaml"** file and navigate to your parent stack's **"template.yaml"**file. Use the **AWS::CloudFormation::Include** resource to include your nested stack's template file. For example:

```
Resources:
  MyNestedStack:
    Type: 'AWS::CloudFormation::Include'
    Properties:
      Location: my-nested-stack/template.yaml
```
This code block defines an include resource named **"MyNestedStack"** that includes the CloudFormation template located at my-nested-stack/template.yaml.

Deploy your parent stack using the aws cloudformation deploy command, and verify that your nested stack was created by navigating to the CloudFormation console and finding the stack with the name **"my-nested-stack"**. You should see all of the resources defined in your nested stack's "template.yaml" file.

In summary, using nested stacks with AWS CloudFormation allows you to create complex infrastructures that are easy to manage and update. With the AWS SAM Python package, defining nested stacks is straightforward and simple. By following the steps outlined in this blog post, you'll be well on your way to creating robust and scalable AWS infrastructures.





