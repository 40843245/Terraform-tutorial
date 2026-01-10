# CH3 -- locals.md
## CH3-1 -- define a local variable
To define a local variable, define a block with `locals` type.

syntax:

```
# define a variable named `<variable-name>` with type `<variable-type>` and default value `<variable-value>`
variable "<variable-name>" {
  type    = <variable-type>
  default = <variable-value>
}
```

Replace `<variable-name>` to `variable name`, `<variable-type>` to `variable type`, and `<variable-value>` to default value.

## CH2-2 -- access a local vairable
Since all defined local variables will be stored in `local` object, to access a local variable named `<variable-name>`

```
local.<variable-name>
```

Replace `<variable-name>` to `variable name`
