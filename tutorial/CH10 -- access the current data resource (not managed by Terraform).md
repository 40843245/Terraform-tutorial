# CH10 -- access the current data resource (not managed by Terraform)
## objectives
You will learn how to

  + access the current available data resource that are not managed by Terraform

## CH10-1 -- access the current available data resource that are not managed by Terraform
### `data` block
In `data` block, current available data resource that are not managed by Terraform can be accessed, but it can't be modified. 

Data resources are readonly.

syntax:

```
data "<data-resource-want-to-be-accessed>" "<alias-name>" {
}
```

Replace `<data-resource-want-to-be-accessed>` to the data resource that you want to access.

Replace `<alias-name>` to a descriptive name to the access of data resource.
