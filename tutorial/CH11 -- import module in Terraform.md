# CH11 -- import module in Terraform
## objectives
You will learn how to 

  + import module in Terraform

## CH11-1 -- import module in Terraform
### `module` block
To import external-defined module in `*.tf` file,

you can use `module` block

syntax:

```
module "<alias-name>" {
  source = "<module-path>"
  # ... pass the variable defined in the external-defined module
}
```

Replace `<alias-name>` to the alias name of imported module.

Replace `<module-path>` relative to
