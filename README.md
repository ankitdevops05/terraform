# terraform

### Test comment

This repo is comprised of terraform code used to create AWS infrastructure for Sandata.

For now, terraform plans and applies are being run from your local CLI. We'll be transitioning this to a VCS-backed run in the near future.

## Creating a new workspace

- Create a new folder with a generic name. Don't use environment-specific naming to identify what your terraform code is going to do
- Copy `tfc.tf` and `providers.tf` into your new directory. You can grab these files from just about any existing workspace
- In your `tfc.tf` file, change `prefix` in the backend block to your folder name, followed by a hyphen ("-")
- Create a new workspace for an environment by running `terraform workspace create <environment>-<short_region>`. For example, `terraform workspace create rd-ue1` would create a workspace for the `rd` environment that belongs to the `us-east-1` region.
  - **Do not stray from this naming convention and PLEASE check your spelling.**
- Make sure you have your new workspace selected: `terraform workspace select rd-ue1`

## How do I run a plan/apply for a specific workspace?

- `cd` to the appropriate directory
- Run `terraform init` if needed
- Ensure you're on the correct workspace using `terraform workspace list`
  - If you're not, select the correct workspace with `terraform workspace select <workspace>`
- Run `terraform plan` and `terraform apply` like normal

### Workspaces that is up to date without drift
  - alt-evv-dataintake-sqs - VCS and modules upgrade done!
  - apigw-logging-01 - VCS and modules upgrade done !
  - ec2-rabbit - VCS and modules upgrade done !
  - ecr-01 - VCS and modules upgrade done !
  - emailhandler-01 - VCS and modules upgrade done !
  - freeradius-01 - VCS and modules upgrade done !
  - kms-app-secret-encryption - VCS and modules upgrade done !
  - mnt-dbtools-01 - VCS and modules upgrade done !
  - nuance - VCS and modules upgrade done !
  - tfc-configuration - VCS and modules upgrade done !
  - vpc-network -
  - vpclink-01 - VCS and modules upgrade done !
  - ec2-newrelic - VCS and modules upgrade done !
  - amp-dlm - VCS and modules upgrade done !
  - systems-manager Matt - VCS and modules upgrade done !
  - sd-sftp Danny - VCS and modules upgrade done !
  - s3-static-smc-doc-central - VCS and modules upgrade done !
  - cognito-opensam-01 - VCS and modules upgrade done !
  - cognito-ordermanager-01 - VCS and modules upgrade done !
  - order-manager-sqs-file-processing - VCS and modules upgrade done !
  - kms-apply-to-encrypt-secret - VCS and modules upgrade done !
  - fms-waf-prod2 - VCS and modules upgrade done !
  - fms-waf-uat - VCS and modules upgrade done !
  - fms-waf-qa - VCS and modules upgrade done !
  - fms-waf-rd - VCS and modules upgrade done !
  - elasticache-redis-01 - VCS and modules upgrade done !
  - alb-proxy-lambda-opensam-01 - Vu it's for opensam alb
  - amp-ssr-01 Matt/Omotayo
  - amp-db-01 - VCS and modules upgrade done !
  - amp-db-03 - VCS and modules upgrade done !
  - amp-db-04 - VCS and modules upgrade done !
  - amp-db-05 - VCS and modules upgrade done !
  - amp-db-06 - VCS and modules upgrade done !
  - amp-db-07 - VCS and modules upgrade done !
  - s3-visit-capture ->  - VCS and modules upgrade done !
  - s3-interfaces - Vu, it's working fine - VCS and modules upgrade done !
  - s3-interfaces-replication - Vu, it's working fine, this is temp repo for S3 migration
  - s3-static-am - Vu, it's working fine
  - lamda-app-auth-etl-nc-converter - Vu, it's working fine - VCS and modules upgrade done !
  - lamda-app-auth-check-new-features - Vu, it's working fine - VCS and modules upgrade done !
  - amp-db-05 - MW/OD - Yet to Apply code changes to Production
  - eks-cluster-01 -  Matt/- Omotayo - VCS and modules upgrade done !
  - aws-back-up-01 Matt - VCS and modules upgrade done !
  - amp-db-06 - MW/OD
  - ddb-entity-status - Matt
  - dms-iam-roles - VCS and modules upgrade done !
  - domo-support-ec2 - VCS and modules upgrade done !
  - cwl-s3-exporter - VCS and modules upgrade done !
  - amp-web-01 - To Apply to Prod2-ue1 - VCS and modules upgrade done !
  - eks-cluster-xl-01 Matt/Omotayo  - VCS and modules upgrade done !
  - eks-cluster-02 Matt/Omotayo - VCS and modules upgrade done !
  - eks-fargate-cluster-01 Matt-Omotayo - VCS and modules upgrade done !
  - rds-mysql-smc-01 Danny  - VCS and modules upgrade done !
  - order-manager  Danny
  - rds-idm-mysql-01 Danny - yet to Apply changes - VCS and modules upgrade done !
  - flight-resources-01  - VCS and modules upgrade done !
  - map-webapp - VCS and modules upgrade done !
  - mcop-sftp Danny
  - eks-api-endpoints - VCS and modules upgrade done !
  - am2-docdb Omotayo - VCS and modules upgrade done !
  - open-billing-s3-static - VCS and modules upgrade done !
  - s3-visit-capture - VCS and modules upgrade done !
  - eks-apigw-deployment-release - VCS and modules upgrade done !
  - s3-static-smc-manual Vu - VCS and modules upgrade done !


### Workspaces plans, but requires drift correction
  - domo-dwh Danny
  - security-baseline Danny



### Workspaces status unknown
  - _DANNY_clientvpn-admin-01
  - _MISSING_VARS_vpncertsß-01/

## IGNORE THIS COMMENT, This is to test documents template
  - Starting from v1.0, this module requires [Terraform Provider for AWS](https://github.com/terraform-providers/terraform-provider-aws) v4.0 or later. [Version 1.0 Upgrade Guide](./docs/upgrade-1.0.md) described the recommended procedure after the upgrade.

## License

See LICENSE for full details.

## Pre-commit hooks

1. Install dependencies
pre-commit
terraform-docs required for terraform_docs hooks. GNU awk is required if using terraform-docs older than 0.8.0 with Terraform 0.12.
TFLint required for terraform_tflint hook.
TFSec required for terraform_tfsec hook.
coreutils required for terraform_validate hook on macOS (due to use of realpath).
checkov required for checkov hook.
terrascan required for terrascan hook.
or build and use the Docker image locally as mentioned below in the Run section.


### Install dependencies

* [`pre-commit`](https://pre-commit.com/#install)
* [`terraform-docs`](https://github.com/segmentio/terraform-docs) required for `terraform_docs` hooks.
* [`TFLint`](https://github.com/terraform-linters/tflint) required for `terraform_tflint` hook.

#### MacOS

```bash
brew install pre-commit gawk terraform-docs tflint tfsec coreutils checkov terrascan
brew tap git-chglog/git-chglog
brew install git-chglog

```
#### Once you have the above install you need to initialize pre-commit locally.

```bash
pre-commit install

```