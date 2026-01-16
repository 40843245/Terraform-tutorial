# CH5 -- environment variable
## objectives
You will learn how to override an environment variable.

Also, you will know the overriding precedence of an environment variable.

## CH5-1 -- overriding precedence of an environment variable
The overriding precedence (from lowest to highest) of an environment variable is as follows. In same overrding precedence, the latter one it reads, it will override the previous one. 

1. pollute environment variable to this session in this parent shell
2. setting environment variable in `terraform.tfvars`
3. setting environment variable in `terraform.tfvars.json`
4. setting environment variable in `*.auto.tfvars`, `*.auto.tfvars.json` (according to file name, sort them with alphabetically ascendant order, so that `00.auto.tfvars.json` will override `00.auto.tfvars` )
5. use command-line flags in `terraform apply` command. Assigning enviroment variable with `-var` option, assigning file name with `-var-file` (it will parse it from left to right)

## CH5-2 -- override an environment variable
Defining a variable named `<variable-name>` (replace `<variable-name>` as a valid identifier) in `*.tf` will define a variable named `TF_VAR_<variable-name>` by `Terraform parser` when executing `terraform apply` command.

Assigning a variable named `<variable-name>` (replace `<variable-name>` as a valid identifier) in `terraform.tfvars` `terraform.tfvars.json`, `*.auto.tfvars`, `*.auto.tfvars.json` will also assign a variable named `TF_VAR_<variable-name>` by `Terraform parser` when executing `terraform apply` command.

Look at examples for details.
