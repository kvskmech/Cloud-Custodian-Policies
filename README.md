# Cloud-Custodian-Policies
Cloud Custodian Policies to clean up and optimize your AWS environment



Policy can be run with the following command

custodian run --config=ebs-unattached-mark.yml --output-dir=./data --region=us-east-1 

resources.json file will be created which will contain the filtered resources.

To run in another account by assuming cross-account role.

custodian run --config=ebs-unattached-mark.yml --output-dir=./data --region=us-east-1 --assume=arn:aws:iam::1234578011:role/CloudCustodian_Role


Cloud Custodian also can provision lambda for the policies which will be triggered in response to cloudwatch events.

Please refer the Official Documentation.

https://capitalone.github.io/cloud-custodian/docs/policy/lambda.html


