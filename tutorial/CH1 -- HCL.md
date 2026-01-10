# CH1 -- HCL (Hashicorp Terraform Configuration)
## CH1-1 -- syntax format
syntax format:

```
<BLOCK-TYPE> "<BLOCK-LABEL-1>" "<BLOCK LABEL-2>" {
   <IDENTIFIER> = <EXPRESSION>
}
```

or

```
<BLOCK-TYPE> "<BLOCK-LABEL-2>" {
   <IDENTIFIER> = <EXPRESSION>
}
```

Replace `<BLOCK-TYPE>` to type of block, `<BLOCK-LABEL-1>` to data or resouce type, and `<BLOCK-LABEL-2>` to variable name or user-predefined name.

Example:

```
# define a variable named `str1` with type string and default value `string1`
variable "str1" {
  type    = string
  default = "string1"
}
```
