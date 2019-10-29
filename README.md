## How to use CI/CD to deploy and configure AWS security services with Terraform

This is sample code for the accompanying AWS Security Blog post How to use CI/CD to deploy and configure AWS security services with Terraform. A CodeBuild buildspec.yml and terraform config files to deploy a Global Web ACL & sample rules are provided.

#### Solutions Architecture
![Architecture](https://github.com/aws-samples/aws-security-services-with-terraform/blob/master/Architecture.jpg)
1.	Push your artifacts, Terraform configuration files and a build specification to a CodePipeline source
2.	CodePipeline automatically invokes CodeBuild and downloads the source files
3.	CodeBuild installs and executes Terraform according to our build specification
4.	Terraform stores our state files in S3 and a record of the deployment in DynamoDB
5.	Our WAF Web ACL is deployed and ready for use by our application teams

You can also use other Terraform config files here

## License

This library is licensed under the MIT-0 License. See the LICENSE file.