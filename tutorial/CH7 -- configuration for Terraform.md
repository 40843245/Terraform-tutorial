# CH7 -- configuration for Terraform
## objectives
You will learn how to

  + configure requirements for Terraform

## CH7-1 -- configure requirements for Terraform
### `terraform` block
`terraform` block contains the configureations and its requirements for Terraform

syntax:

```
terraform {
# ... define more configurations and its requirements
}
```

| attributes | description |
| :-- | :-- |
| `required_version` | The version of Terraform needed to configure Terraform. |

| subsection | description |
| :-- | :-- |
| `required_providers` | specify provider's version |
| `backend` | specify storage location of State |
