[![License](https://img.shields.io/badge/License-Apache-blue.svg)](https://github.com/boldlink/terraform-aws-docdb/blob/main/LICENSE)
[![Latest Release](https://img.shields.io/github/release/boldlink/terraform-aws-docdb.svg)](https://github.com/boldlink/terraform-aws-docdb/releases/latest)
[![Build Status](https://github.com/boldlink/terraform-aws-docdb/actions/workflows/update.yaml/badge.svg)](https://github.com/boldlink/terraform-aws-docdb/actions)
[![Build Status](https://github.com/boldlink/terraform-aws-docdb/actions/workflows/release.yaml/badge.svg)](https://github.com/boldlink/terraform-aws-docdb/actions)
[![Build Status](https://github.com/boldlink/terraform-aws-docdb/actions/workflows/pre-commit.yaml/badge.svg)](https://github.com/boldlink/terraform-aws-docdb/actions)
[![Build Status](https://github.com/boldlink/terraform-aws-docdb/actions/workflows/pr-labeler.yaml/badge.svg)](https://github.com/boldlink/terraform-aws-docdb/actions)
[![Build Status](https://github.com/boldlink/terraform-aws-docdb/actions/workflows/module-examples-tests.yaml/badge.svg)](https://github.com/boldlink/terraform-aws-docdb/actions)
[![Build Status](https://github.com/boldlink/terraform-aws-docdb/actions/workflows/checkov.yaml/badge.svg)](https://github.com/boldlink/terraform-aws-docdb/actions)
[![Build Status](https://github.com/boldlink/terraform-aws-docdb/actions/workflows/auto-merge.yaml/badge.svg)](https://github.com/boldlink/terraform-aws-docdb/actions)
[![Build Status](https://github.com/boldlink/terraform-aws-docdb/actions/workflows/auto-badge.yaml/badge.svg)](https://github.com/boldlink/terraform-aws-docdb/actions)

[<img src="https://avatars.githubusercontent.com/u/25388280?s=200&v=4" width="96"/>](https://boldlink.io)

# Terraform  module example of complete and most common configuration

### Running this example
The makefile contained in this example is optimized for linux paths and the main purpose is to run this example stack including creating supporting resources.

```console
make tests
```
* Clean example stack & supporting resources:
```console
make tfdestroy
```

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 0.14.11 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | >=4.60.0 |
| <a name="requirement_random"></a> [random](#requirement\_random) | >=3.2.0 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | 5.28.0 |
| <a name="provider_random"></a> [random](#provider\_random) | 3.5.1 |

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_complete_cluster"></a> [complete\_cluster](#module\_complete\_cluster) | ./../../ | n/a |
| <a name="module_external_parameter_group"></a> [external\_parameter\_group](#module\_external\_parameter\_group) | ./../../ | n/a |
| <a name="module_kms_key"></a> [kms\_key](#module\_kms\_key) | boldlink/kms/aws | n/a |

## Resources

| Name | Type |
|------|------|
| [aws_docdb_cluster_parameter_group.external](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/docdb_cluster_parameter_group) | resource |
| [aws_docdb_cluster_snapshot.snapshot](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/docdb_cluster_snapshot) | resource |
| [random_password.master_password](https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/password) | resource |
| [random_string.master_username](https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/string) | resource |
| [aws_subnet.database](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/subnet) | data source |
| [aws_subnets.database](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/subnets) | data source |
| [aws_vpc.supporting](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/vpc) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_prefix"></a> [prefix](#input\_prefix) | Prefix for the resource name | `string` | `"external"` | no |
| <a name="input_tags"></a> [tags](#input\_tags) | Tags to apply to the created resources | `map(string)` | <pre>{<br>  "Department": "DevOps",<br>  "Environment": "examples",<br>  "InstanceScheduler": true,<br>  "LayerId": "cExample",<br>  "LayerName": "cExample",<br>  "Owner": "Boldlink",<br>  "Project": "Examples",<br>  "user::CostCenter": "terraform-registry"<br>}</pre> | no |

## Outputs

No outputs.
<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->

## Third party software
This repository uses third party software:
* [pre-commit](https://pre-commit.com/) - Used to help ensure code and documentation consistency
  * Install with `brew install pre-commit`
  * Manually use with `pre-commit run`
* [terraform 0.14.11](https://releases.hashicorp.com/terraform/0.14.11/) For backwards compatibility we are using version 0.14.11 for testing making this the min version tested and without issues with terraform-docs.
* [terraform-docs](https://github.com/segmentio/terraform-docs) - Used to generate the [Inputs](#Inputs) and [Outputs](#Outputs) sections
  * Install with `brew install terraform-docs`
  * Manually use via pre-commit
* [tflint](https://github.com/terraform-linters/tflint) - Used to lint the Terraform code
  * Install with `brew install tflint`
  * Manually use via pre-commit

#### BOLDLink-SIG 2023
