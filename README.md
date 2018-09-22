# Cloud-Custodian-Policies
Cloud Custodian Policies to clean up your AWS environment

custodian validate <policy file> will validate the yaml configuration file

Policy can be run with the following command

custodian run --config=ebs-unattached-mark.yml --output-dir ./data --region=us-east-1 

Filtered resurces will be created in the resources.json file

To run in another account by assuming cross-account role

custodian run --config=ebs-unattached-mark.yml -s ./data --region=us-east-1 --assume=arn:aws:iam::1234578011:role/CloudCustodian_Role


Cloud Custodian also can provision lambda for the policies which will be triggered in response to cloudwatch events.

Please refer the Official Documentation

https://capitalone.github.io/cloud-custodian/docs/policy/lambda.html


