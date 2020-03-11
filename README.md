# Semantix Challenge

Code challenge for Semantix by Níckolas Goline

## Challenge specs

Publication of a CI/CD environment with the following systems:

* Jenkins;
* Nexus;
* SonnarQube;

Specs:

* The environment should be created on a cloud instance using Terraform script;
  * the environment must have an Up and Down script between 8am and 8pm.
* The instance must be multi-cloud, working on AWS, GCP and Azure.
* The systems must be created by docker-compose, having:
  * System-wide expose ports;
  * Persisted volumes;
  * If any problem occur, the containers must self restart.

## Running my code

You must have [AWS CLI](https://aws.amazon.com/cli/?nc1=h_ls) installed and configured.

You must have an SSH key named ```deployer-key``` already configured on AWS and saved on ```~/.ssh/deployer-key.pub```.

To publish the environment execute the following code from this folder:

```bash
terraform apply
```

## Notes

I was able to create a script for AWS only due to not having an active account for testing in Azure or GCP.
