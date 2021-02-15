# Sops into Google Cloud Platform

![Tfsec](https://github.com/nlamirault/terraform-google-sops/workflows/Tfsec/badge.svg)

## Terraform versions

Use Terraform `>= 0.14.0` minimum and Terraform Provider Google `3.54+`.

These types of resources are supported:

* [google_service_account](https://www.terraform.io/docs/providers/google/r/google_service_account.html)
* [google_kms_key_ring](https://registry.terraform.io/providers/hashicorp/google/latest/docs/data-sources/kms_key_ring)
* [google_kms_crypto_key](https://registry.terraform.io/providers/hashicorp/google/latest/docs/data-sources/kms_crypto_key)
* [google_project_iam_binding](https://registry.terraform.io/providers/hashicorp/google/latest/docs/resources/google_project_iam)
* [google_service_account_iam_member](https://registry.terraform.io/providers/hashicorp/google/latest/docs/resources/google_service_account_iam#google_service_account_iam_member)

## Usage

```hcl
module "sops" {
  source  = "nlamirault/sops/google"
  version = "1.0.0"
  
  project = var.project

  keyring_location = var.keyring_location

  namespace       = var.namespace
  service_account = var.service_account
}
```

and variables :

```hcl
project = "foo-prod"

region = "europe-west1"

##############################################################################
# Sops

namespace       = "storage"
service_account = "sops"

keyring_location = "europe-west1"
```

## Documentation
