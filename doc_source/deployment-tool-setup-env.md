--------

Do you want to deploy your \.NET applications to AWS in just a few simple clicks? Try our new [\.NET CLI tooling](https://www.nuget.org/packages/AWS.Deploy.CLI/) for a simplified deployment experience\! Read our [blog post](https://aws.amazon.com/blogs/developer/reimagining-the-aws-net-deployment-experience/) and submit your feedback on [GitHub](https://github.com/aws/aws-dotnet-deploy)\!

 [ ![\[Image NOT FOUND\]](http://docs.aws.amazon.com/sdk-for-net/v3/developer-guide/images/BannerButton.png) ](https://github.com/aws/aws-dotnet-deploy/)

For additional information, see the section for the [deployment tool](https://docs.aws.amazon.com/sdk-for-net/v3/developer-guide/deployment-tool.html) in this guide\.

--------

# Setting up your environment<a name="deployment-tool-setup-env"></a>


****  

|  | 
| --- |
| This is prerelease documentation for a feature in preview release\. It is subject to change\. | 

The following sections show you how to set up your environment to run the deployment tool\.

## Node\.js<a name="deployment-tool-setup-node"></a>

The deployment tool requires the [AWS Cloud Development Kit \(CDK\)](https://docs.aws.amazon.com/cdk/latest/guide/), and the AWS CDK requires [Node\.js](https://nodejs.org/en/download/) version 10\.13\.0 or later \(excluding versions 13\.0\.0 through 13\.6\.0\)\. To see which version of Node\.js you have installed, run the following command at the command prompt or in a terminal:

```
node --version
```

**Note**  
If the AWS CDK isn't installed on your machine or if the AWS CDK that's installed is earlier than the required minimum version \(1\.95\.2\), the deployment tool will install a temporary and "private" copy of the CDK that will be used only by the tool, leaving the global configuration of your machine untouched\.  
If instead you want to install the AWS CDK, see [Install the AWS CDK](https://docs.aws.amazon.com/cdk/latest/guide/getting_started.html#getting_started_install) in the [AWS Cloud Development Kit \(CDK\) Developer Guide](https://docs.aws.amazon.com/cdk/latest/guide/)

## \.NET Core and \.NET<a name="deployment-tool-setup-env-dotnet"></a>

Your application must be built from \.NET Core 3\.1 or later \(for example, \.NET Core 3\.1, \.NET 5\.0, etc\.\)\. To see what version you have, run the following on the command prompt or in a terminal:

```
dotnet --version
```

For information about how to install or update \.NET, see [https://dotnet\.microsoft\.com/](https://dotnet.microsoft.com/)\.

## \(Optional\) Docker<a name="deployment-tool-setup-env-docker"></a>

If you plan to deploy your application to Amazon Elastic Container Service \(Amazon ECS\) using AWS Fargate, you must have Docker installed where you run the deployment tool\. For more information, see [https://docs\.docker\.com/engine/install/](https://docs.docker.com/engine/install/)\.

## \(Linux and macOS\) ZIP CLI<a name="deployment-tool-setup-env-zip"></a>

The ZIP CLI is used when creating ZIP packages for deployment bundles\. It is used to maintain Linux file permissions\.