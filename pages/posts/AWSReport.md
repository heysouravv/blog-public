---
title: AWS CodeReport
date: 2023/04/16
description: Amazon Web Services just released a new AI code completion tool called AWS CodeWhisperer.
tag: AWS
slug: aws-bedrock-release
author: Sourav Padhi
---
## Introduction and Competition in the Development Tooling Space

In April 2023, the development tooling space race is heating up with a plethora of tools competing to offer the best code generation and AI capabilities. One of the latest entrants is Amazon Web Services (AWS), which has just launched a new code generation tool called Code Whisperer. This tool competes with GitHub Co-Pilot, which is powered by Microsoft and OpenAI. However, unlike Co-Pilot, Code Whisperer is 100% free for everyone. In addition to Code Whisperer, AWS has also released a new web service called Bedrock that provides access to large foundational models on AWS infrastructure.

## The Features of Code Whisperer and Comparison with Co-Pilot

Code Whisperer can be installed as a VS Code or JetBrains extension and generates code by understanding the context of the project. It does not suggest as much code as Co-Pilot but is extremely useful for generating simple patterns such as phone numbers. Code Whisperer also has a transparency feature that provides a reference to the code in the training data when producing its own code, which is not available in Co-Pilot.

Code Whisperer also includes security scans that can check web applications for OWASP issues and analyze smart contracts. It provides 50 scans per month, and this feature is not available in Co-Pilot.

## AWS's Foundational Models and ML Training EC2 Instances

AWS has launched Bedrock, which provides access to foundational models on AWS infrastructure. These models include stability AI stable diffusion, LLMs like **AI 21 Labs Jurassic models**, and two of AWS's own foundational models for text and image processing called [Titan](https://aws.amazon.com/bedrock/titan/). Uploading labeled images to S3 is all that is required to build something custom using these models, and it can be done with as few as 20 images.

AWS has also made its new ML training EC2 instances generally available. These instances are based on inference chips that can train machine learning models at about 50% of the normal cost on EC2. It is now possible to train your own LLM from scratch for only $5 million, half of the cost of traditional training on EC2.

## Conclusion and the Future of AI Programming

AWS's Code Whisperer is a significant addition to the development tooling space and is on par with Co-Pilot. Its transparency and security features make it stand out. In addition, AWS's launch of Bedrock and ML training EC2 instances democratizes access to foundational models and makes it possible to train LLMs at a lower cost. The future of AI programming looks promising, and the development tooling space race is far from over.

---
- [AWS BedRock Release](https://aws.amazon.com/bedrock/)