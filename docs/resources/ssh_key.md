---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "juju_ssh_key Resource - terraform-provider-juju"
subcategory: ""
description: |-
  Resource representing an SSH key.
---

# juju_ssh_key (Resource)

Resource representing an SSH key.

## Example Usage

```terraform
resource "juju_ssh_key" "mykey" {
  model   = juju_model.development.name
  payload = "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQC1I8QDP79MaHEIAlfh933zqcE8LyUt9doytF3YySBUDWippk8MAaKAJJtNb+Qsi+Kx/RsSY02VxMy9xRTp9d/Vr+U5BctKqhqf3ZkJdTIcy+z4hYpFS8A4bECJFHOnKIekIHD9glHkqzS5Vm6E4g/KMNkKylHKlDXOafhNZAiJ1ynxaZIuedrceFJNC47HnocQEtusPKpR09HGXXYhKMEubgF5tsTO4ks6pplMPvbdjxYcVOg4Wv0N/LJ4ffAucG9edMcKOTnKqZycqqZPE6KsTpSZMJi2Kl3mBrJE7JbR1YMlNwG6NlUIdIqVoTLZgLsTEkHqWi6OExykbVTqFuoWJJY3BmRAcP9H3FdLYbqcajfWshwvPM2AmYb8V3zBvzEKL1rpvG26fd3kGhk3Vu07qAUhHLMi3P0McEky4cLiEWgI7UyHFLI2yMRZgz23UUtxhRSkvCJagRlVG/s4yoylzBQJir8G3qmb36WjBXxpqAGHfLxw05EQI1JGV3ReYOs= user@somewhere"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `model` (String) The name of the model to operate in.
- `payload` (String) SSH key payload.

### Read-Only

- `id` (String) The ID of this resource.

## Import

Import is supported using the following syntax:

```shell
# Keys can be imported with the username of the key
$ terraform import juju_ssh_key.dev-user dev-user
```