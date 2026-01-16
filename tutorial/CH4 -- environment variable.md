# CH4 -- environment variable
## objectives
You will learn how to override an environment variable.

Also, you will know the overriding precedence of an environment variable.

## CH4-1 -- overriding precedence of an environment variable
The overriding precedence (from lowest to highest) of an environment variable is as follows. In same overrding precedence, the latter one it reads, it will override the previous one. 

1. pollute environment variable to this session in this parent shell
2. setting environment variable in `terraform.tfvars`
3. setting environment variable in `terraform.tfvars.json`
4. setting environment variable in `*.auto.tfvars`, `*.auto.tfvars.json` (according to file name, sort them with alphabetically ascendant order, so that `00.auto.tfvars.json` will override `00.auto.tfvars` )
5. use command-line flags in `terraform apply` command. Assigning enviroment variable with `-var` option, assigning file name with `-var-file` (it will parse it from left to right)
