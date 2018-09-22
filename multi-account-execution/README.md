c7n-org is the tool to execute cloud custodian policies for multiple accounts.


Installation:  pip install c7n-org

c7n-org needs accounts configuration file which contains the account and the role information.

Example:

c7n-org run -c accounts.yml -u policy.yml -t type:prod

The above policy will be run in all the accounts that are tagged with type:prod.

We can also execute the policies by passing the account name as below.

c7n-org run -c accounts.yml -u policy.yml -a account-1

We can also run the custom script across all the accounts by invoking run-script command. c7n-org will autmatically set up the environment for the account in which the script will execute.

Please refer here for more information.

https://github.com/capitalone/cloud-custodian/tree/master/tools/c7n_org
