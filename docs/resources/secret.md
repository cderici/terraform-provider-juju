---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "juju_secret Resource - terraform-provider-juju"
subcategory: ""
description: |-
  A resource that represents a Juju secret.
---

# juju_secret (Resource)

A resource that represents a Juju secret.

## Example Usage

```terraform
resource "juju_secret" "this" {
  model = juju_model.development.name
  name  = "this_secret_name"
  value = {
    key1 = "value1"
    key2 = "value2"
  }
  info = "This is the secret"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `model` (String) The model in which the secret belongs.
- `value` (Map of String, Sensitive) The value map of the secret. There can be more than one key-value pair.

### Optional

- `info` (String) The description of the secret.
- `name` (String) The name of the secret.

### Read-Only

- `secret_id` (String) The ID of the secret.

## Import

Import is supported using the following syntax:

```shell
# Secrets can be imported by using the URI as in the juju show-secrets output.
# Example:
# $juju show-secret secret-name
# coh2uo2ji6m0ue9a7tj0:
#   revision: 1
#   owner: <model>
#   name: secret-name
#   created: 2024-04-19T08:46:25Z
#   updated: 2024-04-19T08:46:25Z
$ terraform import juju_secret.secret-name coh2uo2ji6m0ue9a7tj0
```