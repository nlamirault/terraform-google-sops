# Sops into Google Cloud Platform

![Tfsec](https://github.com/nlamirault/terraform-google-sops/workflows/Tfsec/badge.svg)

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

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
