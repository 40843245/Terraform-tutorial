# CH4 -- assigning an enviroment variable variable
## objectives
You will learn how to

  + assign an enviroment variable variable defined in `*.tf file

## CH4-1 -- assigning an enviroment variable variable defined in `*.tf` file
### setting environment variable in shell
Since the Terraform parse will try to remove the prefix `TF_VAR_` for all environment variable in this session of this shell and then parse it 

(if the environment variable in this session after removal matches the environment variable defined in `*.tf` file) or it will throw a runtime-time error

when executing `terraform apply` command,

you can set the variable named `TF_VAR_<variable-name>` (replace `<variable-name>` to the name of variable defined in `*.tf` file) in this session of shell.

For example:

In terminal, executing

```
TF_VAR_variable1="variable1"
terraform init
terraform plan
terraform apply
```

will override the variable named `variable1` to `variable1` (if it is defined in `*.tf` file) in this session.

> [!NOTE]
> The behavior is ONLY applied to this session as when this session dispears the environment variables set in this session will dispear.

### terraform.tfvars in this directory
You can assign the environment variable in `terraform.tfvars` file under this directory.

### terraform.tfvars.json in this directory
You can assign the environment variable in `terraform.tfvars.json` file under this directory.

### *.auto.tfvars in this directory
You can assign the environment variable in `*.auto.tfvars` file under this directory.

### *.auto.tfvars.json in this directory
You can assign the environment variable in `*.auto.tfvars.json` file under this directory.

### command line args in `terraform apply` command
You can use command line args `-var` followed by key-value pair to assign an environment variable in `terraform apply` command.

syntax:

```
terraform apply -var="<environment-variable-name>=<value>"
```

Replace `<environment-variable-name>` to an environment variable name.

Replace `<value>` to the value to set an environment variable named `<environment-variable-name>`.

> [!NOTE]
> Be careful to overrding precedence.
>
> When the environment variable is override many times,
>
> the highest overriding precedence will win.
>
> See CH5 for more details.

> [!NOTE]
> When the variable is NOT overridden, it will use default value (in `default` attribute) if it has, or the shell will prompt you to enter value if it doesn't have (which is bad scenario for CI/CD) 
