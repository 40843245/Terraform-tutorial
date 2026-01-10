# CH2 -- variables
## CH2-1 -- define a variable
To define a variable, define a block with `variable` type.

syntax:

```
# define a variable named `<variable-name>` with type `<variable-type>` and default value `<variable-value>`
variable "<variable-name>" {
  type    = <variable-type>
  default = <variable-value>
}
```

Replace `<variable-name>` to `variable name`, `<variable-type>` to `variable type`, and `<variable-value>` to default value.

## CH2-2 -- access a vairable
Since all defined variables will be stored in `var` object, to access a variable named `<variable-name>`

```
var.<variable-name>
```

Replace `<variable-name>` to `variable name`
