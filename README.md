# CodePipeline
CI/CD demo using CodePipeline

## VPC and Support Services
Core networking and support applications for the DevOps environment

### OpenVPN
Allows for connection to the internal DevOps environment

### DNS Server
Allows for the use of custom domain names to reach DevOps internal applications
#### Adding a DNS record
1. Download the DNS_Server.json template
2. Add a parameter to capture the private IP address of your server. You can also use the new [import value function](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-importvalue.html)
3. Modify the DNSInstance Userdata and add a line within the PowerShell block following the format:

`"Add-DnsServerResourceRecordA -IPv4Address ", { "Ref" : "JenkinsPrivateIP" }, " -Name jenkins -ZoneName devops.internal -TimeToLive 3600\n",`

Replace jenkins with the new name for your server and replace the IPv4Address parameter with a reference to your app's private IP 

## Jenkins
Continuous integration tool 

# Supplementary Applications (Separate Repositories)

## Chef

## Fugue

## Terraform

# Future Considerations

## Docker

## Ansible

## AWS CodePipeline

## AWS CodeDeploy

## Splunk

## Datadog

